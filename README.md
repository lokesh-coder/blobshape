# Blob shape generator

Generate unique and fixed shaope blobs for web apps.

## Installation

```shell
npm i blobshape
```

## Usage

### Generate random blob

```js
import blobshape from "blobshape";

const { path, seedValue } = blobshape();
const svg = `<svg viewBox="0 0 100 100"><path d=${path} /></svg>`;

// seedValue - returns id string, later it can be used to get same shape
```

### Get fixed shape blob

Set `seed` value to get same fixed shape

```js
import blobshape from "blobshape";

const { path } = blobshape({ seed: "6-6-7171" });
const svg = `<svg viewBox="0 0 100 100"><path d=${path} /></svg>`;
```

### Config

`growth` - Minimum size of the blob in percentage. More the smaller more the randomness.

`edges` - Total nodes to create a shape. Increasing this value will add complexity to the shape.

`size` - SVG blob path size

```js
import blobshape from "blobshape";

const { path } = blobshape({ size: 300, growth: 6, edges: 6, seed: null });
const svg = `<svg viewBox="0 0 100 100"><path d=${path} /></svg>`;
```

## Demo

To see live action of this package check [blobs.app](http://blobs.app) and you can find the source code for that in [github repo](https://github.com/lokesh-coder/blobs.app).

## License

MIT
