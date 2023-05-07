---
id: Scene
slug: scene
---

The `Scene` interface represents a scene in the game. A scene typically contains game objects and manages their lifecycle.

<br/>

## Definition

```ts
interface Scene {
  load(data?: any): void;
  unload(): void;
  update(deltaTime: number): void;
  draw(context: CanvasRenderingContext2D)
}
```

<br/>

## Methods

### load

- Parameters:
  - `data` (optional)
    - Type: `any`
- Return type: `void`

The `load` method is called when the scene is loaded. It is responsible for initializing the scene and its game objects.

### unload

- Return type: `void`

The unload method is called when the scene is unloaded. It is responsible for cleaning up resources and releasing memory used by the scene and its game objects.

### update

- Parameters:
  - `deltaTime`
    - Type: `number`
- Return type: `void`

The method to update the state of a scene, called once per frame. `deltaTime` is the time elapsed since the last frame.

### draw

- Parameters:
  - `context`
    - Type: `CanvasRenderingContext2D`
- Return type: `void`

The method to draw the scene on the given 2D rendering context.