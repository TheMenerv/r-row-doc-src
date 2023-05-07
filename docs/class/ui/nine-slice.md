---
id: NineSlice
slug: nine-slice
---

The `NineSlice` class is used for drawing nine-slice images on a canvas.

<br/>

## Constructor

```ts title="prototype"
constructor(area: Rectangle, leftLimit: number, rightLimit: number, topLimit: number, bottomLimit: number, imageName: string, mode: NineSliceMode = NineSliceMode.Stretch, scale: Point = new Point(1, 1))
```

### Properties

- `area`
  - Type: `Rectangle`
  - The area to draw the nine-slice image.

- `leftLimit`
  - Type: `number`
  - The left limit of the nine-slice image.

- `rightLimit`
  - Type: `number`
  - The right limit of the nine-slice image.

- `topLimit`
  - Type: `number`
  - The top limit of the nine-slice image.

- `bottomLimit`
  - Type: `number`
  - The bottom limit of the nine-slice image.

- `imageName`
  - Type: `string`
  - The name of the image to draw.

- `mode`
  - Type: `NineSliceMode`
  - Default value: `NineSliceMode.Stretch`
  - The mode to draw the nine-slice image.

- `scale`
  - Type: `Point`
  - Default value: `ew Point(1, 1)`
  - The scale of the nine-slice image.

### Examples

```ts
const nineSlice = new NineSlice(
  new Rectangle(new Point(0, 0), new Point(100, 100)),
  10,
  10,
  10,
  10,
  'myImage',
  NineSliceMode.Stretch,
  new Point(1, 1)
);
```

```ts
const nineSlice = new NineSlice(
  new Rectangle(new Point(0, 0), new Point(100, 100)),
  10,
  10,
  10,
  10,
  'myImage',
);
```

<br/>

## Getters & Setters

### area

- Type: `rectangle`

The area to draw the nine-slice image.

<br/>

## Methods

### draw

```ts title="prototype"
draw(context: CanvasRenderingContext2D): void;
```

Draws the nine slice.

#### Parameters

- `context`
  - Type: `CanvasRenderingContext2D`
  - The canvas rendering context.

#### Return

`void`

#### Example

```ts
nineSlice.draw(context);
```