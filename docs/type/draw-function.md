---
id: DrawFunction
slug: draw-function
---

The `DrawFunction` type represents the function that is called every frame to draw an object in the game.

<br/>

## Definition

```ts
type DrawFunction = (ctx: CanvasRenderingContext2D) => void;
```

<br/>

## Parameters

- `ctx`
  - Type: `CanvasRenderingContext2D`
  - The canvas rendering context on which the object will be drawn.

## Return Value

- `void`