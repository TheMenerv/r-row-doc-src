---
id: Line
slug: line
---

The `Line` class represents a Line in 2D space.

<br/>

## Constructor

```ts title="prototype"
constructor(start: Point, end: Point, options: LineOptions = {})
```

### Properties

- `start`
  - Type: `Point`
  - The start point of the line.

- `end`
  - Type: `Point`
  - The end point of the line.

- `options` (optional)
  - Type: `LineOptions`
  - Default value: `{}`
  - The options for the line

<br/>

## Getters

### length

- Type: `number`

The length of the line.

### center

- Type: `Point`

The center of the line.

### angle

- Type: `number`

The angle of the line.

<br/>

## Methods

### setOptions

```ts title="prototype"
setOptions(options: LineOptions): Circle
```

Set the options of the line.

#### Parameters

- `options`
  - Type: `LineOptions`
  - The circle options.

#### Return

`Line` The line with the new options.

#### Example

```ts
const line = new Line(/* ... */);
line.setOptions({ color: 'red', weight: 2 });
```

<br/>

### toArray

```ts title="prototype"
toArray(): [number, number, number, number]
```

Converts a line to an array.

#### Return

`[number, number, number, number]` Array with 4 numbers, the two first are the start position of the line and the two remaining are the end position of the line.

#### Example

```ts
const line = new Line(new Point(10, 10), new Point(20, 20));
const array = line.toArray();
```

<br/>

### equals

```ts title="prototype"
equals(line: Line): boolean
```

Checks if the line is equal to another line.

#### Parameters

- `line`
  - Type: `Line`
  - The line to compare with

#### Return

`boolean` Whether the lines are equal.

#### Example

```ts
const line1 = new Line(new Point(10, 10), new Point(20, 20));
const line2 = new Line(new Point(10, 10), new Point(20, 20));
const line3 = new Line(new Point(10, 10), new Point(20, 30));
line1.equals(line2); // true
line1.equals(line3); // false
line2.equals(line3); // false
```

<br/>

### isContainsPoint

```ts title="prototype"
isContainsPoint(point: Point, tolerance: number = 0.1): boolean
```

Checks if the line contains a point.

#### Parameters

- `point`
  - Type: `Point`
  - The point to check

- `tolerance` (optional)
  - Type: `number`
  - Default value: `0.1`
  - The tolerance to use

#### Return

`boolean` Whether the line contains the point.

#### Example

```ts
const line = new Line(new Point(10, 10), new Point(20, 20));
line.isContainsPoint(new Point(15, 15)); // true
```

<br/>

### isIntersectsWithLine

```ts title="prototype"
isIntersectsWithLine(line: Line, tolerance: number = 0.1): boolean
```

Checks if the line intersects with another line.

#### Parameters

- `line`
  - Type: `Line`
  - The line to check.

- `tolerance` (optional)
  - Type: `number`
  - Default value: `0.1`
  - The tolerance to use

#### Return

`boolean` Whether the lines intersect.

#### Example

```ts
const line1 = new Line(new Point(10, 10), new Point(20, 20));
const line2 = new Line(new Point(10, 20), new Point(20, 10));
line1.isIntersectsWithLine(line2); // true
```

<br/>

### getIntersectionsWithLine

```ts title="prototype"
getIntersectionsWithLine(line: Line, tolerance: number = 0.1): Point[]
```

Get the intersections with another line

#### Parameters

- `line`
  - Type: `Line`
  - The line to check.

- `tolerance` (optional)
  - Type: `number`
  - Default value: `0.1`
  - The tolerance to use.

#### Return

`Point[]` The intersections.

#### Example

```ts
const line1 = new Line(new Point(10, 10), new Point(20, 20));
const line2 = new Line(new Point(10, 20), new Point(20, 10));
const intersections = line1.getIntersectionsWithLine(line2);
```

<br/>

### isIntersectsWithRectangle

```ts title="prototype"
isIntersectsWithRectangle(rectangle: Rectangle): boolean
```

Check if the line intersects with a rectangle.

#### Parameters

- `rectangle`
  - Type: `Rectangle`
  - The rectangle to check.

#### Return

`boolean` Whether the line intersects with the rectangle.

#### Example

```ts
const line = new Line(new Point(10, 10), new Point(20, 20));
const rectangle = new Rectangle(new Point(10, 20), new Point(20, 10));
line.isIntersectsWithRectangle(rectangle); // true
```

<br/>

### getIntersectionsWithRectangle

```ts title="prototype"
getIntersectionsWithRectangle(rectangle: Rectangle): Point[]
```

Get the intersection point of the line with a rectangle.

#### Parameters

- `rectangle`
  - Type: `Rectangle`
  - The rectangle to check.

#### Return

`Point[]` The intersection points.

#### Example

```ts
const line = new Line(new Point(10, 10), new Point(20, 20));
const rectangle = new Rectangle(new Point(10, 20), new Point(20, 10));
const points = line.getIntersectionsWithRectangle(rectangle);
```

<br/>

### isInRectangle

```ts title="prototype"
isInRectangle(rectangle: Rectangle): boolean
```

Check if the line is in a rectangle.

#### Parameters

- `rectangle`
  - Type: `Rectangle`
  - The rectangle to check.

#### Return

`boolean` Whether the line is in the rectangle.

#### Example

```ts
const line = new Line(new Point(10, 10), new Point(20, 20));
const rectangle = new Rectangle(new Point(10, 20), new Point(20, 10));
line.isInRectangle(rectangle); // true
```

<br/>

### isIntersectsWithCircle

```ts title="prototype"
isIntersectsWithCircle(circle: Circle, tolerance: number = 0.1): boolean
```

Check if the line intersects with a circle.

#### Parameters

- `circle`
  - Type: `Circle`
  - The circle to check.

- `tolerance`
  - Type: `number`
  - Default value: `0.1`
  - The tolerance to use.

#### Return

`boolean` Whether the line intersects with the circle.

#### Example

```ts
const line = new Line(new Point(10, 10), new Point(20, 20));
const circle = new Circle(new Point(15, 15), 5);
line.isIntersectsWithCircle(circle); // true
```

<br/>

### getIntersectionsWithCircle

```ts title="prototype"
getIntersectionsWithCircle(circle: Circle, tolerance: number = 0.1): Point | null
```

Get the intersection point of the line with a circle.

#### Parameters

- `circle`
  - Type: `Circle`
  - The circle to check.

- `tolerance`
  - Type: `number`
  - Default value: `0.1`
  - The tolerance to use.

#### Return

`Point | null` The intersection point or null if the line doesn't intersect with the circle.

#### Example

```ts
const line = new Line(new Point(10, 10), new Point(20, 20));
const circle = new Circle(new Point(15, 15), 5);
const point = line.getPointFromIntersectsWithCircle(circle);
```

<br/>

### isInCircle

```ts title="prototype"
isInCircle(circle: Circle): boolean
```

Check if the line is in a circle

#### Parameters

- `circle`
  - Type: `Circle`
  - The circle to check.

#### Return

`Point | null` Whether the line is in the circle.

#### Example

```ts
const line = new Line(new Point(10, 10), new Point(20, 20));
const circle = new Circle(new Point(15, 15), 5);
line.isInCircle(circle); // true
```

<br/>

### clone

```ts title="prototype"
clone(): Line
```

Get a copy of line.

#### Return

`Line` The copy.

#### Example

```ts
const line = new Line(new Point(10, 10), new Point(20, 20));
const line2 = line.clone();
```

<br/>

### draw

```ts title="prototype"
draw(ctx: CanvasRenderingContext2D): void
```

Draw the Line.

#### Parameters

- `ctx`
  - Type: `CanvasRenderingContext2D`
  - The canvas context.

#### Return

`void`

#### Example

```ts
const line = new Line(new Point(10, 10), new Point(20, 20));
line.draw(ctx);
```

<br/>

## Static methods

### fromArray

```ts title="prototype"
static fromArray(array: [number, number, number, number]): Line
```

Creates a line from an array

#### Parameters

- `array`
  - Type: `[number, number, number number]`
  - Array with 4 numbers, the two first are the start position of the line and the two remaining are the end position of the line.

#### Return

`Line` The line.

#### Example

```ts
const line = Line.fromArray([10, 10, 20, 20]);
```