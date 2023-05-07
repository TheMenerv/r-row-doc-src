---
id: Mouse
slug: mouse
---

The `Mouse` class is a singleton class that handles mouse input.

:::info
Prefer to get the unique instance of this service from the `ServiceContainer` like:

```ts
const mouse = ServiceContainer.mouse;
```
:::

<br/>

## Getters

### instance

- Type: `Mouse`

Get the instance of mouse service.

### position

- Type: `Point`

Get the position of the mouse on the canvas.

<br/>

## Methods

### isDown

```ts title="prototype"
isDown(button: MouseButton): boolean;
```

Check if a button is down.

#### Parameters

- `button`
  - Type: `MouseButton`
  - The button to check.

#### Return

`boolean` - `true` if the button is down, `false` otherwise.

#### Example

```ts
ServiceContainer.Mouse.isDown(MouseButton.Left);
```

<br/>

### isUp

```ts title="prototype"
isUp(button: MouseButton): boolean;
```

Check if a key is up.

#### Parameters

- `button`
  - Type: `MouseButton`
  - The button to check.

#### Return

`boolean` - `true` if the button is up, `false` otherwise.

#### Example

```ts
ServiceContainer.Mouse.isUp(MouseButton.Left);
```

<br/>

### isJustDown

```ts title="prototype"
isJustDown(button: MouseButton): boolean;
```

Check if a button is just down during the current frame.

#### Parameters

- `button`
  - Type: `MouseButton`
  - The button to check.

#### Return

`boolean` - `true` if the button is just down down, `false` otherwise.

#### Example

```ts
ServiceContainer.Mouse.isJustDown(MouseButton.Left);
```

<br/>

### isJustUp

```ts title="prototype"
isJustUp(button: MouseButton): boolean;
```

Check if a button is just up during the current frame.

#### Parameters

- `button`
  - Type: `MouseButton`
  - The button to check.

#### Return

`boolean` - `true` if the button is just up, `false` otherwise.

#### Example

```ts
ServiceContainer.Mouse.isJustUp(MouseButton.Left);
```

<br/>

### setCursor

```ts title="prototype"
setCursor(image: string, offset: Point | number): Mouse;
```

Set the cursor image.

#### Parameters

- `image`
  - Type: `string`
  - The image to use for the cursor.

- `offset`
  - Type: `Point | number`
  - The offset of the cursor.

#### Return

`Mouse` The mouse service.

#### Examples

```ts
ServiceContainer.Mouse.setCursor('cursor.png', 0);
```

```ts
ServiceContainer.Mouse.setCursor('cursor.png', new Point(0, 0));
```