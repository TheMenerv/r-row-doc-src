---
id: GameLoop
slug: game-loop
---

The `GameLoop` class is a singleton that handles the game loop. It manages update and render subscribers, as well as calculating the delta time and frame rate.

:::info
Prefer to get the unique instance of this service from the `ServiceContainer` like:

```ts
const gameLoop = ServiceContainer.gameLoop;
```
:::

<br/>

## Getters

### instance

- Type: `GameLoop`

Returns the singleton instance of the `GameLoop` class.

### FPS

- Type: `number`

Returns the current frames per second (FPS) as a number.

<br/>

## Methods

### setFreezeLimit

```ts title="prototype"
setFreezeLimit(limit: number): GameLoop
```

Sets the freeze limit in seconds.

#### Parameters

- `limit`
  - Type: `number`
  - The freeze limit in seconds

#### Return

`GameLoop` The instance of the GameLoop class.

#### Example

```ts
ServiceContainer.GameLoop.setFreezeLimit(0.1);
```

<br/>

### subscribeToUpdate

```ts title="prototype"
subscribeToUpdate(subscriber: UpdateFunction): GameLoop
```

Subscribes a function to the update loop.

#### Parameters

- `subscriber`
  - Type: `UpdateFunction`
  - The function to subscribe

#### Return

`GameLoop` The instance of the GameLoop class.

#### Example

```ts
ServiceContainer.GameLoop.subscribeToUpdate((deltaTime) => {
  console.log(`deltaTime: ${deltaTime}`);
});
```

<br/>

### unsubscribeFromUpdate

```ts title="prototype"
unsubscribeFromUpdate(subscriber: UpdateFunction): GameLoop
```

Unsubscribes a function from the update loop.

#### Parameters

- `subscriber`
  - Type: `UpdateFunction`
  - The function to unsubscribe

#### Return

`GameLoop` The instance of the GameLoop class.

#### Example

```ts
const updateFunction = (deltaTime) => {
  console.log(`deltaTime: ${deltaTime}`);
};
const gameLoop = ServiceContainer.GameLoop;
gameLoop.subscribeToUpdate(updateFunction);
//...
gameLoop.unsubscribeFromUpdate(updateFunction);
```

<br/>

### subscribeToPreRender

```ts title="prototype"
subscribeToPreRender(subscriber: DrawFunction): GameLoop
```

Subscribes a function to the pre-render loop.

#### Parameters

- `subscriber`
  - Type: `DrawFunction`
  - The function to subscribe

#### Return

`GameLoop` The instance of the GameLoop class.

#### Example

```ts
ServiceContainer.GameLoop.subscribeToPreRender((ctx) => {
  ctx.fillStyle = 'red';
  ctx.fillRect(0, 0, 100, 100);
});
```

<br/>

### unsubscribeFromPreRender

```ts title="prototype"
unsubscribeFromPreRender(subscriber: DrawFunction): GameLoop
```

Unsubscribes a function to the pre-render loop.

#### Parameters

- `subscriber`
  - Type: `DrawFunction`
  - The function to unsubscribe

#### Return

`GameLoop` The instance of the GameLoop class.

#### Example

```ts
const preRenderFunction = (ctx) => {
  ctx.fillStyle = 'red';
  ctx.fillRect(0, 0, 100, 100);
};
const gameLoop = ServiceContainer.GameLoop;
gameLoop.subscribeToPreRender(preRenderFunction);
//...
gameLoop.unsubscribeFromPreRender(preRenderFunction);
```

<br/>

### subscribeToPostRender

```ts title="prototype"
subscribeToPostRender(subscriber: DrawFunction): GameLoop
```

Subscribes a function to the post-render loop.

#### Parameters

- `subscriber`
  - Type: `DrawFunction`
  - The function to subscribe

#### Return

`GameLoop` The instance of the GameLoop class.

#### Example

```ts
ServiceContainer.GameLoop.subscribeToPostRender((ctx) => {
  ctx.fillStyle = 'red';
  ctx.fillRect(0, 0, 100, 100);
});
```

<br/>

### unsubscribeFromPostRender

```ts title="prototype"
unsubscribeFromPostRender(subscriber: DrawFunction): GameLoop
```

Unsubscribes a function from the post-render loop.

#### Parameters

- `subscriber`
  - Type: `DrawFunction`
  - The function to unsubscribe

#### Return

`GameLoop` The instance of the GameLoop class.

#### Example

```ts
const postRenderFunction = (ctx) => {
  ctx.fillStyle = 'red';
  ctx.fillRect(0, 0, 100, 100);
};
const gameLoop = ServiceContainer.GameLoop;
gameLoop.subscribeToPostRender(postRenderFunction);
//...
gameLoop.unsubscribeFromPostRender(postRenderFunction);
```