---
id: ButtonOptions
slug: button-options
---

The `ButtonOptions` interface represents the options for configuring a button in the game.

<br/>

## Definition

```ts
interface ButtonOptions {
  nineSlices?: Map<ClickableState, NineSlice>;
  sprites?: Map<ClickableState, Sprite>;
}
```

<br/>

## Properties

:::caution
You must provide one of these properties!
:::

### nineSlices

- Type: `Map<ClickableState, NineSlice>` (optional)

A map of `ClickableState` to `NineSlice` instances, which can be used to define the appearance of the button in different states using a nine-slice technique.

### sprites

- Type: `Map<ClickableState, Sprite>` (optional)

A map of `ClickableState` to `Sprite` instances, which can be used to define the appearance of the button in different states using sprites.
