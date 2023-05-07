---
id: Clickable
slug: clickable
---

The `Clickable` class provide an area with features like a button.

<br/>

## Constructor

```ts title="prototype"
constructor(area: Rectangle, disabled: boolean = false)
```

### Properties

- `area`
  - Type: `Rectangle`
  - The clickable area.

- `disabled`
  - Type: `boolean`
  - Default value: `false`
  - Whether the clickable is disabled.

<br/>

## Getters

### area

- Type: `Rectangle`

The area of the clickable (relative to the canvas).

### isDisabled

- Type: `boolean`

Whether the clickable is disabled.

### isClicked

- Type: `boolean`

Whether the clickable is clicked.

### isPressed

- Type: `boolean`

Whether the clickable is pressed.

### isHovered

- Type: `boolean`

Whether the clickable is hovered.

### isReleased

- Type: `boolean`

Whether the clickable is released.

<br/>

## Methods

### disable

```ts title="prototype"
disable(disabled: boolean = true): void
```

Disables the clickable.

#### Parameters

- `disabled`
  - Type: `boolean`
  - Default value: `true`
  - Whether the clickable is disabled.

#### Return

`void`

#### Example

```ts
const clickable = new Clickable(new Rectangle(0, 0, 100, 100));
clickable.disable();
```

<br/>

### enable

```ts title="prototype"
enable(enabled: boolean = true): void
```

Enables the clickable.

#### Parameters

- `enabled`
  - Type: `boolean`
  - Default value: `true`
  - Whether the clickable is enabled.

#### Return

`void`

#### Example

```ts
const clickable = new Clickable(new Rectangle(0, 0, 100, 100));
clickable.enable();
```

<br/>

### update

```ts title="prototype"
update(deltaTime: number): void
```

Updates the clickable state.

#### Parameters

- `deltaTime`
  - Type: `number`
  - The time since the last update.

#### Return

`void`

#### Example

```ts
const clickable = new Clickable(new Rectangle(0, 0, 100, 100));
//...
clickable.update(deltaTime);
```