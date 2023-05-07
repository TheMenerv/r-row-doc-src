---
id: SpriteSheet
slug: spritesheet
---

`SpriteSheet` is a class that extends the `Sprite` class. It allows the management of sprite sheet animations.

:::info
This class extends from `Sprite`.

**All getters, setters and methods from `Sprite` are available here!**
:::

<br/>

## Constructor

```ts title="prototype"
constructor(imageName: string, frameSize: Point);
```

### Properties

- `imageName`
  - Type: `string`
  - The name of the image to use.

- `frameSize`
  - Type: `Point`
  - The size of a single frame.

### Example

```ts
const spriteSheet = new SpriteSheet('myImage', new Point(32, 32));
```

<br/>

## Getters

### currentAnimation

- Type: `SpriteSheetAnimation`

The current animation.

### currentAnimationName

- Type: `string`

The name of the current animation.

### currentAnimationFrame

- Type: `number`

The current frame of the current animation.

### isAnimationEnded

- Type: `boolean`

Whether the animation has ended.

<br/>

## Methods

### addAnimation

```ts title="prototype"
addAnimation(name: string, animation: SpriteSheetAnimation): SpriteSheet;
```

Adds an animation to the sprite sheet.

#### Parameters

- `name`
  - Type: `string`
  - The name of the animation.

- `animation`
  - Type: `SpriteSheetAnimation`
  - The animation to add.

#### Return

`SpriteSheet` The spritesheet.

#### Example

```ts
const animation = new SpriteSheetAnimation(/* ... */);
const spriteSheet = new SpriteSheet(/* ... */);
spriteSheet.addAnimation('walk', animation);
```

<br/>

### resetAnimation

```ts title="prototype"
resetAnimation(): SpriteSheet;
```

Resets the current animation.

#### Return

`SpriteSheet` The spritesheet.

#### Example

```ts
const spriteSheet = new SpriteSheet(/* ... */);
spriteSheet.addAnimation('attack', /* ... */);
spriteSheet.setAnimation('attack');
//...
spriteSheet.resetAnimation();
```

<br/>

### setAnimation

```ts title="prototype"
setAnimation(name: string, reset: boolean = true): SpriteSheet;
```

Sets the current animation.

#### Parameters

- `name`
  - Type: `string`
  - The name of the animation.

- `reset` (optional)
  - Type: `boolean`
  - Default value: `true`
  - Whether to reset the animation.

#### Return

`SpriteSheet` The spritesheet.

#### Example

```ts
const spriteSheet = new SpriteSheet(/* ... */);
spriteSheet.addAnimation('walk', /* ... */);
spriteSheet.setAnimation('walk');
```

<br/>

### update

```ts title="prototype"
update(deltaTime: number): void;
```

Updates the sprite sheet.

#### Parameters

- `deltaTime`
  - Type: `number`
  - The time since the last update.

#### Return

`void`

#### Example

```ts
const spriteSheet = new SpriteSheet(/* ... */);
spriteSheet.addAnimation('walk', /* ... */);
spriteSheet.setAnimation('walk');
//...
spriteSheet.update(deltaTime);
```

<br/>

### draw

```ts title="prototype"
draw(context: CanvasRenderingContext2D): void;
```

Draws the sprite sheet.

#### Parameters

- `context`
  - Type: `CanvasRenderingContext2D`
  - The context to draw on.

#### Return

`void`

#### Example

```ts
const spriteSheet = new SpriteSheet(/* ... */);
spriteSheet.addAnimation('walk', /* ... */);
spriteSheet.setAnimation('walk');
//...
spriteSheet.draw(context);
```