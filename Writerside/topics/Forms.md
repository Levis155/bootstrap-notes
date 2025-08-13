# Forms

Bootstrap's form system provides a collection of classes and layout utilities to make building responsive, accessible, and consistent forms easy.

**Key Points:**

- Supports vertical, horizontal, and inline form layouts. 
- Provides custom-styled form controls (inputs, selects, checkboxes, radios, switches, etc.). 
- Includes validation states and helper text. 
- Works with flexbox and grid system for positioning.

## Form Layout Options

### Vertical Forms (default)

In this layout each control is stacked 

```html
<form>
  <div class="mb-3">
    <label for="name" class="form-label">Name</label>
    <input type="text" class="form-control" id="name">
  </div>
  <div class="mb-3">
    <label for="email" class="form-label">Email</label>
    <input type="email" class="form-control" id="email">
  </div>
  <button type="submit" class="btn btn-primary">Submit</button>
</form>

```

### Horizontal Forms

Labels and inputs are placed side-by-side using the grid system.

```html
<form>
  <div class="row mb-3">
    <label for="name" class="col-sm-2 col-form-label">Name</label>
    <div class="col-sm-10">
      <input type="text" class="form-control" id="name">
    </div>
  </div>
  <button class="btn btn-primary">Submit</button>
</form>

```

### Inline Forms

Compact, inline display for quick inputs.

```html
<form class="row g-3 align-items-center">
  <div class="col-auto">
    <label for="inlineFormInput" class="visually-hidden">Name</label>
    <input type="text" class="form-control" id="inlineFormInput" placeholder="Name">
  </div>
  <div class="col-auto">
    <button class="btn btn-primary">Submit</button>
  </div>
</form>

```

## Form Controls

Bootstrap styles most HTML5 form controls.

### Text Inputs

```html
<input type="text" class="form-control" placeholder="Enter text">

```

### Selects

```html
<select class="form-select">
  <option>Option 1</option>
  <option>Option 2</option>
</select>

```

### Checkboxes & Radios

```html
<div class="form-check">
  <input class="form-check-input" type="checkbox" id="check1">
  <label class="form-check-label" for="check1">Check me</label>
</div>

<div class="form-check">
  <input class="form-check-input" type="radio" name="exampleRadios" id="radio1">
  <label class="form-check-label" for="radio1">Option 1</label>
</div>

```

### Switches

```html
<div class="form-check form-switch">
  <input class="form-check-input" type="checkbox" id="flexSwitch">
  <label class="form-check-label" for="flexSwitch">Toggle me</label>
</div>

```

### File Inputs

```html
<input class="form-control" type="file">

```

### Range Sliders

```html
<input type="range" class="form-range" min="0" max="5">

```

## Sizing & Disabled States

### Large & Small Inputs

```html
<input class="form-control form-control-lg" type="text" placeholder="Large input">
<input class="form-control form-control-sm" type="text" placeholder="Small input">

```

### Disabled 

```html
<input class="form-control" type="text" disabled placeholder="Disabled">

```

## Input Groups

Used to prepend or append text/icons/buttons to inputs.

```html
<div class="input-group mb-3">
  <span class="input-group-text">@</span>
  <input type="text" class="form-control" placeholder="Username">
</div>

<div class="input-group">
  <input type="text" class="form-control" placeholder="Recipient's username">
  <button class="btn btn-outline-secondary">Send</button>
</div>

```

## Floating Labels

Labels float above the imput when focused or filled.

```html
<div class="form-floating mb-3">
  <input type="email" class="form-control" id="floatingEmail" placeholder="name@example.com">
  <label for="floatingEmail">Email address</label>
</div>

```

## Form Validation

Bootstrap applies **validation states** with colors and feedback messages.

**Example:**

```html
<form class="needs-validation" novalidate>
  <div class="mb-3">
    <label for="validationCustom01" class="form-label">First name</label>
    <input type="text" class="form-control" id="validationCustom01" required>
    <div class="valid-feedback">Looks good!</div>
    <div class="invalid-feedback">Please enter your first name.</div>
  </div>
  <button class="btn btn-primary" type="submit">Submit</button>
</form>

```

**Validation classes:**

- is-valid 
- is-invalid 
- valid-feedback 
- invalid-feedback