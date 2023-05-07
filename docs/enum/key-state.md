---
id: KeyState
slug: key-state
---

The `KeyState` enum represents the various states of a key in the game.

<br/>

## Definition

```ts
enum KeyState {
  Up = 'up',
  Down = 'down',
  JustUp = 'just_up',
  JustDown = 'just_down',
}
```

<br/>

## Enum Values

- `Up`: The key is up.
- `Down`: The key is down.
- `JustUp`: The key was just released.
- `JustDown`: The key was just pressed.