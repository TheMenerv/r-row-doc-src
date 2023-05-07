---
id: Circle
slug: circle
---

The `Circle` class represents a circle in 2D space.

<br/>

## Constructor

```ts title="prototype"
constructor(position: Point, radius: number, options: CircleOptions = {});
```

### Properties

- `position`
  - Type: `Point`
  - The position of the circle (from the center).

- `radius`
  - Type: `number`
  - The radius of the circle.

- `options` (optional)
  - Type: `CircleOptions`
  - Default value: `{}`
  - The options for the circle

<br/>

## Methods

### setOptions

```ts title="prototype"
setOptions(options: CircleOptions): Circle
```

Set the options of the circle.

#### Parameters

- `options`
  - Type: `CircleOptions`
  - The circle options.

#### Return

`Circle` The circle.

#### Example

```ts
const circle = new Circle(new Point(10, 10), 10);
circle.setOptions({ fillColor: 'red', weight: 2, strokeColor: 'blue' });
```

<br/>

### toArray

```ts title="prototype"
toArray(): [number, number, number]
```

Converts a circle to an array.

#### Return

`[number, number, number]` Array with 3 numbers, the two first are the position of the circle and the third is the radius.

#### Example

```ts
const circle = new Circle(new Point(10, 10), 10);
const array = circle.toArray();
```

<br/>

### equals

```ts title="prototype"
equals(circle: Circle): boolean
```

Checks if the circle is equal to another circle.

#### Parameters

- `circle`
  - Type: `Circle`
  - The circle to compare with

#### Return

`boolean` Whether the circles are equal.

#### Example

```ts
const circle1 = new Circle(new Point(10, 10), 10);
const circle2 = new Circle(new Point(10, 10), 10);
const circle3 = new Circle(new Point(10, 10), 20);
circle1.equals(circle2); // true
circle1.equals(circle3); // false
circle2.equals(circle3); // false
```

<br/>

### isContainsPoint

```ts title="prototype"
isContainsPoint(point: Point): boolean
```

Checks if the circle contains a point.

#### Parameters

- `point`
  - Type: `Point`
  - The point to check

#### Return

`boolean` Whether the circle contains the point.

#### Example

```ts
const circle = new Circle(new Point(10, 10), 10);
circle.isContainsPoint(new Point(12, 12)); // true
```

<br/>

### isIntersectsWithCircle

```ts title="prototype"
isIntersectsWithCircle(circle: Circle): boolean
```

Checks if the circle intersects with another circle.

#### Parameters

- `circle`
  - Type: `Circle`
  - The circle to check.

#### Return

`boolean` Whether the circle intersects with the other circle.

#### Example

```ts
const circle1 = new Circle(new Point(10, 10), 10);
const circle2 = new Circle(new Point(10, 10), 10);
const circle3 = new Circle(new Point(10, 10), 20);
circle1.isIntersectsWithCircle(circle2); // true
circle1.isIntersectsWithCircle(circle3); // true
circle2.isIntersectsWithCircle(circle3); // true
```

<br/>

### isIntersectsWithLine

```ts title="prototype"
isIntersectsWithLine(line: Line): boolean
```

Check if the circle intersects with a line.

#### Parameters

- `line`
  - Type: `Line`
  - The line to check.

#### Return

`boolean` Whether the circle intersects with the line.

#### Example

```ts
const circle = new Circle(new Point(10, 10), 10);
const line = new Line(new Point(0, 0), new Point(20, 20));
circle.isIntersectsWithLine(line); // true
```

<br/>

### getIntersectionsWithLine

```ts title="prototype"
getIntersectionsWithLine(line: Line): Point[]
```

Get the intersections with a line.

#### Parameters

- `line`
  - Type: `Line`
  - The line to get the intersections with.

#### Return

`Point[]` The intersections with the line.

#### Example

```ts
const circle = new Circle(new Point(10, 10), 10);
const line = new Line(new Point(0, 0), new Point(20, 20));
const intersections = circle.getIntersectionsWithLine(line);
```

<br/>

### isIntersectsWithRectangle

```ts title="prototype"
isIntersectsWithRectangle(rectangle: Rectangle): boolean
```

Get the intersections with a line.

#### Parameters

- `rectangle`
  - Type: `Rectangle`
  - The rectangle to check.

#### Return

`boolean` Whether the circle intersects with the rectangle.

#### Example

```ts
const circle = new Circle(new Point(10, 10), 10);
const rectangle = new Rectangle(new Point(0, 0), new Size(20, 20));
circle.isIntersectsWithRectangle(rectangle); // true
```

<br/>

### getIntersectionsWithRectangle

```ts title="prototype"
getIntersectionsWithRectangle(rectangle: Rectangle): Point[]
```

Get the intersections with a line.

#### Parameters

- `rectangle`
  - Type: `Rectangle`
  - The rectangle to get the intersections with.

#### Return

`Point[]` The intersections with the rectangle.

#### Example

```ts
const circle = new Circle(new Point(10, 10), 10);
const rectangle = new Rectangle(new Point(0, 0), new Size(20, 20));
const intersections = circle.getIntersectionsWithRectangle(rectangle);
```

<br/>

### clone

```ts title="prototype"
clone(): Circle
```

Get a copy of circle.

#### Return

`Circle` The copy.

#### Example

```ts
const circle = new Circle(new Point(10, 10), 10);
const clonedCircle = circle.clone();
```

<br/>

### draw

```ts title="prototype"
draw(ctx: CanvasRenderingContext2D): void
```

Draw the circle.

#### Parameters

- `ctx`
  - Type: `CanvasRenderingContext2D`
  - The canvas context.

#### Return

`void`

#### Example

```ts
const circle = new Circle(new Point(10, 10), 10);
//...
circle.draw(ctx);
```

<br/>

## Static methods

### fromArray

```ts title="prototype"
static fromArray(array: [number, number, number]): Circle
```

Creates a circle from an array

#### Parameters

- `array`
  - Type: `[number, number, number]`
  - Array with 3 numbers, the two first are the position of the circle and the third is the radius.

#### Return

`Circle` The circle.

#### Example

```ts
const circle = Circle.fromArray([10, 10, 10]);
```