# React

## Hooks

### isLoading

```js
import { useState } from "react";

function isLoading(action) {
  const [loading, setLoading] = useState(false);

  function doAction(...args) {
    setLoading(true);
    return action(...args).finally(() => setLoading(false));
  };

  return [doAction, loading];
};
```

Example

```js
import {asyncA, asyncB} from './api'

const ComponentWithLoading = () => {
  const [doA, aLoading] = isLoading(asyncA);
  const [doB, bLoading] = isLoading(asyncB);

  useEffect(() => {
    doA();
    doB();
  }, []);

  if (aLoading || bLoading)
    return null; // or some fallback component

  return (
    // ...your real component content
  )
}
```

### isMounted

Useful for async actions, that you don't want to run when the component isn't mounted.

```js
const isMounted = () => {
  const isMounted = useRef(false);

  useEffect(() => {
    isMounted.current = true;
    return () => {
      isMounted.current = false;
    };
  }, []);

  return isMounted;
};
```

Example

```js
function Button ({onClick, ...rest}) {
  const [loading, setLoading] = useState(false);
  const isMounted = isMounted();
  const onClicked = async (e) => {
    setLoading(true);
    await onClick(e);
    isMounted.current && setLoading(false);
  }
  return <button onClick={onClicked} {...rest}/>
}
```
