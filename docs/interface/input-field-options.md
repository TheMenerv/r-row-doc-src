---
id: InputFieldOptions
slug: input-field-options
---

The `InputFieldOptions` interface represents the options for configuring an input field in the game.

<br/>

## Definition

```ts
interface InputFieldOptions {
  type?: InputFieldType;
  placeholder?: string;
  maxLength?: number;
  style?: CSSStyleDeclaration;
}
```

<br/>

## Properties

### type

- Type: `InputFieldType` (optional)

The type of input field (e.g., `text`, `password`, `email`, ...).

### placeholder

- Type: `string` (optional)

The placeholder text displayed in the input field.

### maxLength

- Type: `number` (optional)

The maximum length of the input field.

### style

- Type: `CSSStyleDeclaration` (optional)

The CSS style applied to the input field.