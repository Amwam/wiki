# Flow-to-Ts

List files using flow

```
grep -rnw '<path>' -e '@flow' | awk '{print $1}' | sed -e 's/:1:\/\///'
```

Library for converting:
[https://github.com/Khan/flow-to-ts](https://github.com/Khan/flow-to-ts)

Combined

```sh
FILES=`grep -rnw '<path>' -e '@flow' | awk '{print $1}' | sed -e 's/:1:\/\///'`
flow-to-ts <filepath>  --prettier --write --delete-source

```
