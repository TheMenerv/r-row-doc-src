---
id: SpriteSheetAnimation
slug: spritesheet-animation
---

The `SpriteSheetAnimation` class represents an animation for a sprite sheet.

<br/>

## Constructor

```ts title="prototype"
constructor(frames: number[], speed: number, loop: boolean = true): void;
```

### Parameters

- `frames`
  - Type: `number[]`
  - The frames of the animation.

- `speed`
  - Type: `number`
  - The speed of the animation (in frame per second).

- `loop` (optional)
  - Type: `boolean`
  - Default value: `true`
  - Whether or not the animation should loop.

### Examples

```ts
const animation = new SpriteSheetAnimation([0, 1, 2], 1);
```

```ts
const animation = new SpriteSheetAnimation([0, 1, 2], 1, false);
```

<br/>

## Getters

### frames

- Type: `number[]`

Gets the frames of the animation.

### loop

- Type: `boolean`

Gets whether or not the animation should loop.

### isEnded

- Type: `boolean`

Gets whether or not the animation has ended.

<br/>

## Getters & Setters

### currentFrame

- Type: `number`

Gets or sets the current frame of the animation.

<br/>

## Methods

### reset

```ts title="prototype"
reset(): void;
```

Resets the animation.

#### Return

`void`

#### Example

```ts
const animation = new SpriteSheetAnimation(/* ... */);
//...
animation.reset();
```

<br/>

### update

```ts title="prototype"
update(deltaTime: number): void;
```

Updates the animation.

#### Parameters

- `deltaTime`
  - Type: `number`
  - The time since the last frame.

#### Return

`void`

#### Example

```ts
const animation = new SpriteSheetAnimation(/* ... */);
//...
animation.update(deltaTime);
```