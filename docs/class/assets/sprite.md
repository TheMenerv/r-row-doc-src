---
id: Sprite
slug: sprite
---

The `Sprite` class represents a drawable image.

<br/>

## Constructor

```ts title="prototype"
constructor(name: string);
```

### Properties

- `name`
  - Type: `string`
  - The name of the image to use.

<br/>

## Getters & Setters

### position

- Type: `Point`

The position of the sprite (relative to the canvas).

### size

- Type: `Point`

The size of the sprite.

### scale

- Type: `Point`

The scale of the sprite.

### isVerticalFlipped

- Type: `boolean`

Whether the sprite is vertically flipped.

### isHorizontalFlipped

- Type: `boolean`

Whether the sprite is horizontally flipped.

<br/>

## Methods

### draw

```ts title="prototype"
draw(context: CanvasRenderingContext2D): void;
```

Draws the sprite.

#### Parameters

- `context`
  - Type: `CanvasRenderingContext2D`
  - The context of the canvas to draw.

#### Return

`void`

#### Example

```ts
const sprite = new Sprite('myImage');
sprite.position = new Point(100, 100);
sprite.size = new Point(100, 100);
sprite.scale = new Point(2, 2);
sprite.isVerticalFlipped = true;
sprite.isHorizontalFlipped = true;
//...
const context = ServiceContainer.GameCanvas.context;
sprite.draw(context);
```