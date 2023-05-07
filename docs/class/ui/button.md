---
id: Button
slug: button
---

`Button` is a class that extends the `Clickable` class. It allows the management of buttons.

:::info
This class extends from `Clickable`.

**All getters, setters and methods from `Clickable` are available here!**
:::

<br/>

## Constructor

```ts title="prototype"
constructor(area: Rectangle, options: ButtonOptions, disabled: boolean = false);
```

### Properties

- `area`
  - Type: `Rectangle`
  - The clickable area.

- `options`
  - Type: `ButtonOptions`
  - The button options.

- `disabled`
  - Type: `boolean`
  - Default value: `false`
  - Whether the button is disabled.

### Example

```ts
const options = {
  nineSlices: new Map([
    [ClickableState.Released, new NineSlice(new Rectangle(0, 0, 100, 100), 10, 10, 10, 10)],
    ...
   ]),
}
const button = new Button(new Rectangle(0, 0, 100, 100), options);
```

<br/>

## Methods

### update

```ts title="prototype"
update(deltaTime: number): void;
```

Updates the button.

#### Parameters

- `deltaTime`
  - Type: `number`
  - The time since the last update.

#### Return

`void`

#### Example

```ts
button.update(deltaTime);
```

<br/>

### draw

```ts title="prototype"
draw(context: CanvasRenderingContext2D): void;
```

Draws the button.

#### Parameters

- `context`
  - Type: `CanvasRenderingContext2D`
  - The canvas rendering context.

#### Return

`void`

#### Example

```ts
button.draw(context);
```