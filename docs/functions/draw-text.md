---
id: drawText
slug: draw-text
---

The `drawText` function is used for drawing text on a canvas.

## Prototype

```ts title="prototype"
drawText(context: CanvasRenderingContext2D, text: string, position: Point, options?: DrawTextOptions)
```

### Parameters

- `context`
  - Type: `CanvasRenderingContext2D`
  - The canvas context.

- `text`
  - Type: `string`
  - The text to draw.

- `position`
  - Type: `Point`
  - The position of the text on the canvas.

- `options`
  - Type: `DrawTextOptions`
  - Default value: `undefined`
  - The options for drawing the text.

### Return

`void`

### Default options

- `fillColor`: `'transparent'`
- `align`: `'left'`
- `fontName`: `'Arial'`
- `fontSize`: `'8px'`
- `strokeColor`: `'transparent'`
- `strokeSize`: `0`