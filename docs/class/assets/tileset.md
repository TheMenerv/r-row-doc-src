---
id: TileSet
slug: tileset
---

The `TileSet` class is used for drawing tiles from a tileset image.

<br/>

## Constructor

```ts title="prototype"
constructor(imageName: string, frameSize: Point, scale: Point = new Point(1, 1));
```

### Parameters

- `imageName`
  - Type: `string`
  - The name of the image to use.

- `frameSize`
  - Type: `Point`
  - The size of a single frame.

- `scale` (optional)
  - Type: `Point`
  - Default value: `new Point(1, 1)`
  - The scale of the tile.

### Examples

```ts
const tileSet = new TileSet('myImage', new Point(32, 32));
```

```ts
const tileSet = new TileSet('myImage', new Point(32, 32), new Point(2, 2));
```

<br/>

## Methods

### drawTile

```ts title="prototype"
drawTile(context: CanvasRenderingContext2D, TileId: number, position: Point, useCache?: boolean): void;
```

#### Parameters

- `context`
  - Type: `CanvasRenderingContext2D`
  - The context to draw to on.

- `TileId`
  - Type: `number`
  - The id of the tile to draw.

- `position`
  - Type: `Point`
  - The position to draw the tile at.

- `useCache`
  - Type: `boolean`
  - Default value: `undefined` (disable cache system)
  - Whether or not to use the cache (use the cache improve performances).

#### Return

`void`

#### Example

```ts
const tileSet = new TileSet(/* ... */);
//...
tileSet.drawTile(context, 0, new Point(0, 0));
```