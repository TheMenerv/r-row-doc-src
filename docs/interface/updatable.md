---
id: Updatable
slug: updatable
---

The `Updatable` interface represents an object that can be updated every frame in the game.

<br/>

## Definition

```ts
interface Updatable {
  update: UpdateFunction;
}
```

<br/>

## Methods

### update

- Type: `UpdateFunction`

The update method that should be implemented by any object implementing the `Updatable` interface. This method is responsible for updating the state of the object on each frame.