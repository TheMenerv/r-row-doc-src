---
id: UpdateFunction
slug: update-function
---

The `UpdateFunction` type represents the function that is called every frame to update the state of an object in the game.

<br/>

## Definition

```ts
type UpdateFunction = (deltaTime: number) => void;
```

<br/>

## Parameters

- `deltaTime`
  - Type: `number`
  - The time elapsed since the last frame.

## Return Value

- `void`