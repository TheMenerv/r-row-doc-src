---
id: Getting Started
slug: getting-started
---

## Create a Game

Create a game:

```ts
import { Game } from 'r-row';

const game = new Game();
```

<br/>

## Create Canvas

You can use default canvas options:

```ts
game.createCanvas();
```

<br/>

Or create a Canvas settings object from `CanvasOption` interface:

```ts
import { CanvasOptions } from 'r-row';

const options: CanvasOptions = {
  // your settings here
};
```

and pass it to the `createCanvas` method:

```ts
game.createCanvas(options);
```

<br/>

## Set scene to start with the game (facultative)

If you want use the Scenes system provided by R-Row, you can use this method before starting the game:

```ts
game.startScene(new MySceneClass());
```

A new instance of `MySceneClass` will be start automatically when the game start.

<br/>

## Start the game

```ts
game.start();
```

## Resume

```ts
import { CanvasOption, Game } from 'r-row';
import { MyScene } from './scenes/MyScene';

const option: CanvasOptions = {
  imageSmoothingEnabled: false;
}

const game = new Game()
  .createCanvas(options)
  .startScene(new MyScene())
  .start();
```