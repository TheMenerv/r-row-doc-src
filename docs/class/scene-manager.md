---
id: SceneManager
slug: scene-manager
---

The `SceneManager` class is a singleton that manages scenes. It is responsible for setting the current scene and providing access to it.

:::info
It is possible to not use this class and manage scenes by oneself with their own scene manager using the subscribers of the `GameLoop`.
:::

:::info
Prefer to get the unique instance of this service from the `ServiceContainer` like:

```ts
const sceneManager = ServiceContainer.SceneManager;
```
:::

<br/>

## Getters

### instance

- Type: `SceneManager`

Returns the `singleton` instance of the SceneManager class.

### currentScene

- Type: `Scene | undefined`

Returns the current scene or `undefined` if no scene is set.

<br/>

## Methods

### setScene

```ts title="prototype"
setScene(scene: Scene, data?: any): SceneManager
```

Sets the current scene and optionally passes data to it.

#### Parameters

- `scene`
  - Type: `Scene`
  - The scene to set as the current scene.

- `data` (optional)
  - Type: `any`
  - Optional data to pass to the scene.

#### Return

`void`

#### Examples

```ts
ServiceContainer.setScene(new GameScene());
```

or with data:

```ts
ServiceContainer.setScene(new GameScene(), { difficulty: 1 });
```