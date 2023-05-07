---
id: Drawable
slug: drawable
---

The `Drawable` interface represents an object that can be drawn in the game.

<br/>

## Definition

```ts
interface Drawable {
  draw: DrawFunction;
}
```

<br/>

## Methods

### draw

- Type: `DrawFunction`

The draw method that should be implemented by any object implementing the `Drawable` interface. This method is responsible for rendering the object on the screen.