---
id: InputField
slug: input-field
---

The `InputField` class creates an input field for the user to input text.

:::caution
Don't forget to destroy the `InputField` when necessary!
:::

<br/>

## Constructor

```ts title="prototype"
constructor(area: Rectangle, options?: InputFieldOptions)
```

### Properties

- `area`
  - Type: `Rectangle`
  - The input field area.

- `options`
  - Type: `InputFieldOptions`
  - The input field options.

### Example

```ts
const options = {
  type: InputFieldType.Text,
  placeholder: 'Enter your name',
  maxLength: 10,
  style: {
    color: 'red',
    backgroundColor: 'blue',
  },
};
const inputField = new InputField(new Rectangle(0, 0, 100, 100), options);
```

<br/>

## Getters

### value

- Type: `string`

The value of the input field.

### isSubmittedByEnterKey

- Type: `boolean`

Whether the input field is submitted by Enter key.

<br/>

## Getters & Setters

### area

- Type: `Rectangle`

The area of the input field.

<br/>

## Methods

### getInputElement

```ts title="prototype"
getInputElement(): HTMLInputElement
```

Get the HTMLInputElement of the input field. It's useful for manipulating the input element directly.

#### Return

`HTMLInputElement`

#### Example

```ts
const inputField = new InputField(...);
const input = inputField.getInputElement();
input.value = "Hi!";
```

<br/>

### setOptions

```ts title="prototype"
setOptions(options: InputFieldOptions): void
```

Set the options for the input field.

#### Parameters

- `options`
  - Type: `InputFieldOptions`
  - The options for the input field.

#### Return

`void`

#### Example

```ts
const options = {
  type: InputFieldType.Text,
  placeholder: 'Enter your name',
  maxLength: 10,
  style: {
    color: 'red',
    backgroundColor: 'blue',
  },
};
const inputField = new InputField(...);
inputField.setOptions(options);
```

<br/>

### clear

```ts title="prototype"
clear(): void;
```

Clear the content of input field.

#### Return

`void`

#### Example

```ts
const inputField = new InputField(/* ... */);
//...
inputField.clear();
```

<br/>

### destroy

```ts title="prototype"
destroy(): void;
```

Destroy the input field.

#### Return

`void`

#### Example

```ts
const inputField = new InputField(/* ... */);
//...
inputField.destroy();
```
