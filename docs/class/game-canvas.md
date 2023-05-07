---
id: GameCanvas
slug: game-canvas
---

The `GameCanvas` class is a singleton class that manages the game canvas.

:::info
Prefer to get the unique instance of this service from the `ServiceContainer` like:

```ts
const gameCanvas = ServiceContainer.GameCanvas;
```
:::

<br/>

## Getters

### instance

- Type: `GameCanvas`

Returns the instance of the GameCanvas (Usage of Service Container is recommanded).

### canvas

- Type: `HTMLCanvasElement`

The canvas element.

### context

- Type: `CanvasRenderingContext2D`

The canvas context.

### baseSize

-Type: `Point`

The base size of canvas. This is useful for calculating positions and dimensions.

### scale

- Type: `number`

The scale of the canvas.

### position

- Type: `Point`

The position of the canvas.

<br/>

## Methods

### init

```ts title="Prototype"
init(options?: CanvasOptions): GameCanvas
```

Initialize the canvas.

#### Parameters

- `options` (optional)
  - Type: `CanvasOptions`
  - The options to set the canvas

#### Return

`void`

#### Example

```ts
ServiceContainer.GameCanvas.init();
```

or with custom configuration:

```ts
ServiceContainer.GameCanvas.init({
  size: new Point(800, 600),
  parent: document.body,
  imageSmoothingEnabled: true,
  backgroundColor: '#000'
});
```

<br/>

### fullscreen

```ts title="Prototype"
fullscreen(): GameCanvas
```

Sets the canvas to fullscreen.

#### Return

- Type: `GameCanvas`

The instance of the GameCanvas class.

#### Example

```ts
ServiceContainer.GameCanvas.fullscreen();
```

<br/>

### exitFullscreen

```ts title="Prototype"
exitFullscreen(): GameCanvas
```

Exits fullscreen mode.

#### Return

- Type: `GameCanvas`

The instance of the GameCanvas class.

#### Example

```ts
ServiceContainer.GameCanvas.exitFullscreen();
```

<br/>

### toggleFullscreen

```ts title="Prototype"
toggleFullscreen(): GameCanvas
```

Toggles fullscreen mode.

#### Return

- Type: `GameCanvas`

The instance of the GameCanvas class.

#### Example

```ts
ServiceContainer.GameCanvas.toggleFullscreen();
```

<br/>

### clearScreen

```ts title="Prototype"
clearScreen(): GameCanvas
```

Clears the canvas.

#### Return

- Type: `GameCanvas`

The instance of the GameCanvas class.

#### Example

```ts
ServiceContainer.GameCanvas.clearScreen();
```