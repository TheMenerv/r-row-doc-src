---
id: Game
slug: game
---

The main game class that handles game initialization and startup.

<br/>

## Methods

<br/>

### start

```ts title="prototype"
public start(): Game
```

Starts the game by initializing the game loop, keyboard, mouse, and touch inputs.

#### Example:

```ts
const game = new Game();
game.start();
```

<br/>

### createCanvas

```ts title="prototype"
public createCanvas(canvasOptions?: CanvasOptions): Game
```

Creates the game canvas with the specified options.

- `canvasOptions` (optional): The options for the canvas.

#### Example:

```ts
const game = new Game();
game.createCanvas({ width: 800, height: 600 });
```

<br/>

### startScene

```ts title="Prototype"
public startScene(scene: Scene): Game
```

Adds scenes to the scene manager and selects a scene.

- `scene`: The scene to start.

#### Example:

```ts
const game = new Game();
game.startScene(new GameScene());
```