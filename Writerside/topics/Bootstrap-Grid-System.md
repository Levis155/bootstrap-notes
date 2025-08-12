# Bootstrap Grid System

## What is the Bootstrap Grid System

The grid system in Bootstrap is a flexbox-based layout system that helps you arrange page content into responsive columns and rows.

- It works with 12 columns by default.
- Columns automatically stack on smaller devices and align side-by-side on larger ones (unless you override).
- It’s built on flexbox, so it supports alignment, ordering, and flexible widths.

## Core components of the Grid

<table>
  <thead>
    <tr>
      <th>Component</th>
      <th>Purpose / Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>.container</td>
      <td>Fixed-width (responsive) wrapper that centers page content — width changes at breakpoints to keep readable margins.</td>
    </tr>
    <tr>
      <td>.container-fluid</td>
      <td>Full-width container that always spans the entire viewport width (no fixed max width).</td>
    </tr>
    <tr>
      <td>.row</td>
      <td>Horizontal wrapper for columns. Provides negative margins so column gutters align correctly and handles horizontal layout.</td>
    </tr>
    <tr>
      <td>.col / .col-*</td>
      <td>Column elements that live inside a .row. Use plain .col for equal-width columns or .col-{size}-{n} (e.g., .col-md-6) to set specific widths across breakpoints.</td>
    </tr>
  </tbody>
</table>

### Containers

They're like the "frame" for your grid. Their widths changes automatically at Bootstrap's breakpoints to keep line lengths readable. A container is use when you want consistent margins on the left and right so your design doesn't stretch too wide on large screens.

**Example**

```html
<div class="container">
  <p>This is inside a fixed-width container.</p>
</div>

```

### Container-fluid

This is a full-width container that always spans the entire width of the browser viewport. Unlike .container, it doesn’t cap width at breakpoints — it stays edge-to-edge at all times. It is great for banners, background images, or sections where you want the content or background color to cover the entire width of the screen.

**Example:**

```html
<div class="container-fluid">
  <p>This spans the entire width of the screen.</p>
</div>

```

### row

This is a horizontal wrapper for columns. It applies negative margins on the sides so that the columns inside line up with the container edges, creating proper gutters (spacing between columns).

Always place .col elements inside .row. Columns should never be direct children of .container or .container-fluid.

**Example:**

```html
<div class="row">
  <div class="col">Column 1</div>
  <div class="col">Column 2</div>
</div>

```

### col

These define the actual columns of your grid.

They possess the following behaviors:

- .col without a number → Automatically shares available space equally with other .cols in the same row.
- .col-n (e.g., .col-6) → Takes up a fixed fraction of the row’s 12-column grid (e.g., .col-6 = half the row).\
- .col-{breakpoint}-{n} (e.g., .col-md-4) → Applies that width only from the given breakpoint upward; below it, the column becomes full width unless another class overrides it.

**Example:**

```html
<div class="row">
  <div class="col-4">4 units</div>
  <div class="col-8">8 units</div>
</div>

```

## Breakpoints

Breakpoints are the specific screen widths at which a website's layout changes to adapt to different screen sizes. Bootstrap uses a mobile-first approach, meaning styles apply to the smallest breakpoint by default and are then adjusted for larger screens.

Bootstrap 5 includes 6 default breakpoints:

<table>
  <thead>
    <tr>
      <th>Breakpoint</th>
      <th>Class Infix</th>
      <th>Dimensions</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>X-Small</td>
      <td>None</td>
      <td>&lt;576px</td>
      <td>Extra small devices (portrait phones)</td>
    </tr>
    <tr>
      <td>Small</td>
      <td>sm</td>
      <td>≥576px</td>
      <td>Small devices (landscape phones)</td>
    </tr>
    <tr>
      <td>Medium</td>
      <td>md</td>
      <td>≥768px</td>
      <td>Medium devices (tablets)</td>
    </tr>
    <tr>
      <td>Large</td>
      <td>lg</td>
      <td>≥992px</td>
      <td>Large devices (desktops)</td>
    </tr>
    <tr>
      <td>Extra large</td>
      <td>xl</td>
      <td>≥1200px</td>
      <td>Extra large devices (large desktops)</td>
    </tr>
    <tr>
      <td>Extra extra large</td>
      <td>xxl</td>
      <td>≥1400px</td>
      <td>Extra extra large devices</td>
    </tr>
  </tbody>
</table>

Bootstrap uses specific class prefixes to target different breakpoints:

- col-* - Extra small (xs) - no infix needed (mobile-first)
- col-sm-* - Small devices (≥576px)
- col-md-* - Medium devices (≥768px)
- col-lg-* - Large devices (≥992px)
- col-xl-* - Extra large devices (≥1200px)
- col-xxl-* - Extra extra large devices (≥1400px)

**Example:**

```html
<div class="container">
  <div class="row">
    <div class="col-sm-12 col-md-6 col-lg-4">Column A</div>
    <div class="col-sm-12 col-md-6 col-lg-4">Column B</div>
    <div class="col-sm-12 col-md-12 col-lg-4">Column C</div>
  </div>
</div>

```

Here:
- On small screens: all columns stack (full width). 
- On medium screens: first two share row, third moves below. 
- On large screens: all three fit in one row.

## Column Sizing

### Equal-width columns:

Use .col without a number. Columns automatically divide the available space evenly:

```html
<div class="row">
  <div class="col">Equal</div>
  <div class="col">Equal</div>
</div>

```

### Fixed-width columns

Use .col-{n} where n is 1–12:

```html
<div class="row">
  <div class="col-3">25%</div>
  <div class="col-9">75%</div>
</div>

```

## Auto Layout Columns

Let columns adjust automatically while mixing fixed sizes and flexible widths.

```html
<div class="row">
  <div class="col">Auto</div>
  <div class="col-6">Fixed half</div>
  <div class="col">Auto</div>
</div>

```

The auto columns share the remaining space after the fixed column takes its share.

## Nesting grids

You can place a .row inside a .col to create sub-layouts.

```html
<div class="row">
  <div class="col-8">
    <div class="row">
      <div class="col-6">Nested 1</div>
      <div class="col-6">Nested 2</div>
    </div>
  </div>
  <div class="col-4">Side</div>
</div>

```

## Column Ordering

Use order classes to change the visual order of columns without changing the HTML order.

This swaps their order depending on screen size.

```html
<div class="row">
  <div class="col order-2 order-md-1">First visually</div>
  <div class="col order-1 order-md-2">Second visually</div>
</div>

```

## Alignment

Because the grid is flexbox-based, you can align columns vertically and horizontally.

**Vertical Alignment:**

```html
<div class="row align-items-center">
  <div class="col">Centered vertically</div>
</div>

```

**Horizontal Alignment:**

```html
<div class="row justify-content-center">
  <div class="col-4">Centered horizontally</div>
</div>

```

## Gutters

Gutters are the horizontal and vertical spaces between columns. 
- Controlled with g-* classes (0–5). 
- Default: g-3 (1.5rem horizontal, same vertical).

Examples:

```html
<div class="row g-0">No gutters</div>
<div class="row g-2">Small gutters</div>
<div class="row g-5">Large gutters</div>

```