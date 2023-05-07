---
id: DrawTextOptions
slug: draw-text-options
---

The `DrawTextOptions` interface represents the options for configuring the rendering of text in the game.

<br/>

## Definition

```ts
interface DrawTextOptions {
  fillColor?: string;
  align?: 'right' | 'center' | 'left';
  fontName?: string;
  fontSize?: string;
  strokeColor?: string;
  strokeSize?: number;
}
```

<br/>

## Properties

### fillColor

- Type: `string` (optional)

The fill color of the text.

### align

- Type: `'right' | 'center' | 'left'` (optional)

The text alignment.

### fontName

- Type: `string` (optional)

The name of the font used for the text.

### fontSize

- Type: `string` (optional)

The size of the font, in CSS format (e.g., `16px`, `1em`, ...).

### strokeColor

- Type `string` (optional)

The stroke color of the text.

### strokeSize

- Type: `number` (optional)

The size of the stroke applied to the text.