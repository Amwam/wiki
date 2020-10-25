# React

## Hooks

### isLoading
```js
import {asyncA, asyncB} from './api'

const ComponentWithLoading = () => {
  const [doA, aLoading] = useLoading(asyncA);
  const [doB, bLoading] = useLoading(asyncB);

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
