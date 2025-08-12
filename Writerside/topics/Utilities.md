# Utilities

Bootstrap utilities are single-purpose helper classes that apply a specific style instantly without the need to write custom CSS.

- They follow a consistent naming convention: property-value or property-breakpoint-value. 
- They work responsively — you can apply them for all devices or specific breakpoints.

**Example:**

```html
<p class="text-center text-md-start m-3">Responsive aligned text</p>

```

Here:

- text-center → Centered on all devices. 
- text-md-start → Left-aligned from md (≥768px) upward. 
- m-3 → Applies margin on all sides.

Bootstrap utilities can be grouped into major categories as follows:

## Spacing Utilities

Used for margin (m) and padding (p).

### Syntax

```arduino
{property}{sides}-{breakpoint?}-{size}

```
- **Property:** m(margin) or p(padding)
- **Sides:** t(top), b(bottom), s(start), e(end), x(left&right), y(top & bottom), none(all sides)
- **Breakpoint(optional):** sm, md, lg, xl, xxl
- **size:** 0-5 (0=0, 1=0.25rem, 2=0.5rem, 3=1rem, 4=1.5rem, 5=3rem), or auto

**Examples:**

```html
<div class="p-3">Padding on all sides</div>
<div class="mt-4">Margin top 1.5rem</div>
<div class="px-2">Horizontal padding 0.5rem</div>
<div class="ms-auto">Left margin auto</div>

```

## Text Utilities

Control text alignment, wrapping, transformation, color, and more.

**Common classes:**
- **Alignment:** text-start, text-center, text-end
- **Responsive Alignment:** text-md-center, text-lg-end
- **Transform:** text-lowercase, text-uppercase, text-capitalize
- **Wrap & Truncate:** text-wrap, text-nowrap, text-truncate
- **Font weight & style:** fw-bold, fw-normal, fw-light, fst-italic
- **Line height:** lh-1, lh-sm, lh-base, lh-lg 
- **Text color:** text-primary, text-success, text-danger, text-muted, etc.

**Example:**

```html
<p class="text-uppercase fw-bold text-danger text-md-center">
  Important Warning!
</p>

```

## Display & Visibility utilities

Control how elements appear

**Display classes:**

- d-block, d-inline, d-inline-block, d-flex, d-inline-flex 
- **Responsive:** d-sm-none, d-md-block, d-lg-flex

**Example:**

```html
<div class="d-none d-md-block">Visible on md and larger</div>

```

## Flexbox Utilities

Helps arrange content with flexbox

- **Direction:** flex-row, flex-row-reverse, flex-column, flex-column-reverse
- **Justify content:** justify-content-start, justify-content-center, justify-content-end, justify-content-between, justify-content-around, justify-content-evenly
- **Align items:** align-items-start, align-items-center, align-items-end
-  **Align self:** align-self-start, align-self-center, align-self-end
- **wrap:** flex-wrap, flex-nowrap, flex-wrap-reverse

**Example:**

```html
<div class="d-flex justify-content-between align-items-center">
  <span>Left</span>
  <span>Right</span>
</div>

```

## Background & Border Utilities
**Background colors:** bg-primary, bg-secondary, bg-success, bg-danger, bg-warning, bg-info, bg-light, bg-dark, bg-white, bg-transparent

**Borders:**
- **Add border:** border, border-top, border-end, border-bottom, border-start
- **Remove border:** border-0, border-top-0, etc. 
- **Border colors:** border-primary, border-success, etc.
- **Border radius:** rounded, rounded-top, rounded-circle, rounded-pill, rounded-0

**Example:**
```html
<div class="border border-primary rounded p-3">
    Box with blue border and rounded corners
</div>
 
```

## Sizing Utilities

Control width, height, max/min dimensions.

- **Width:** w-25, w-50, w-75, w-100, w-auto
- **Height:** h-25, h-50, h-75, h-100, h-auto
- **Max/Min:** mw-100 (max width 100%), mh-100 (max height 100%)

**Example:**

```html
<img src="photo.jpg" class="w-50 h-auto">

```

## Position Utilities

Position elements using position and offsets.

- **Position type:** position-static, position-relative, position-absolute, position-fixed, position-sticky 
- **Offsets:** top-0, top-50, bottom-0, start-0, end-0, etc. 
- **Center with translate:** translate-middle

**Example:**

```html
<div class="position-relative">
  <span class="position-absolute top-0 start-100 translate-middle badge bg-danger">1</span>
</div>

```

## Shadows

- shadow-none, shadow-sm, shadow, shadow-lg

**Example:**

```html
<div class="shadow p-3 bg-white">Card with shadow</div>

```

## Overflow

- overflow-auto, overflow-hidden, overflow-visible, overflow-scroll

## Visibility

- visible (default) and invisible (removes visibility but keeps layout space)