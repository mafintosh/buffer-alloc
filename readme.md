# Buffer Alloc

A ponyfill for `Buffer.alloc`, uses native implementation if available.

## Installation

```sh
npm install --save buffer-alloc
```

## Usage

```js
const alloc = require('buffer-alloc')

console.log(alloc(4))
//=> <Buffer 00 00 00 00>

console.log(alloc(6, 0x41))
//=> <Buffer 41 41 41 41 41 41>

console.log(alloc(10, 'linus', 'utf8'))
//=> <Buffer 6c 69 6e 75 73 6c 69 6e 75 73>
```

## API

### alloc(size[, fill[, encoding]])

- `size` &lt;Integer&gt; The desired length of the new `Buffer`
- `fill` &lt;String&gt; | &lt;Buffer&gt; | &lt;Integer&gt; A value to pre-fill the new `Buffer` with. **Default:** `0`
- `encoding` &lt;String&gt; If `fill` is a string, this is its encoding. **Default:** `'utf8'`

Allocates a new `Buffer` of `size` bytes. If `fill` is `undefined`, the `Buffer` will be zero-filled.

## See also

- [buffer-from](https://github.com/LinusU/buffer-from) A ponyfill for `Buffer.from`
- [buffer-alloc-unsafe](https://github.com/LinusU/buffer-alloc-unsafe) A ponyfill for `Buffer.allocUnsafe`
