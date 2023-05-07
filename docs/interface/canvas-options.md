---
id: CanvasOptions
slug: canvas-options
---

The `CanvasOptions` interface represents the options for configuring the game canvas.

<br/>

## Definition

```ts
interface CanvasOptions {
  parent?: HTMLElement;
  size?: Point;
  imageSmoothingEnabled?: boolean;
  imageSmoothingQuality?: ImageSmoothingQuality;
  backgroundColor?: string;
}
```

<br/>

## Properties

### parent

- Type: `HTMLElement` (optional)
  - *Default value: `document.body`*

The parent element to insert the canvas.


### size

- Type: `Point` (optional)
  - *Default value: `new Point(800, 600)`*

The size of the canvas.

### imageSmoothingEnabled

- Type: `boolean`(optional)
  - *Default value: `false`*

Determines whether image smoothing is enabled


### imageSmoothingQuality

- Type: `ImageSmoothingQuality` (optional)
  - *Default value: `high`*

The quality of image smoothing.

*(none effective if `imageSmoothingEnable` is set to `false`)*

### backgroundColor

- Type: `string` (optional)
  - *Default value: `#000000`*

The background color of the canvas.