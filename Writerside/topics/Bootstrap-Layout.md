# Bootstrap Layout

Bootstrap layout is built on components and options for laying out your Bootstrap project, including wrapping containers, a powerful grid system, a flexible media object, and responsive utility classes.

## Containers

Containers are the most basic layout element in Bootstrap and are required when using the default grid system.
They can be chosen from a responsive, fixed-width container (meaning its max-width changes at each breakpoint) or fluid-width (meaning its 100% wide all the time)

```html
<div class="container">
    ...
</div>

<div class="container-fluid">
    ...
</div>
```

## Responsive breakpoints



**Basic Grid example**

```html
<div class="container">
  <div class="row">
    <div class="col-sm-6 col-md-4 col-lg-3">
      <!-- Content -->
    </div>
    <div class="col-sm-6 col-md-4 col-lg-3">
      <!-- Content -->
    </div>
    <div class="col-sm-6 col-md-4 col-lg-3">
      <!-- Content -->
    </div>
    <div class="col-sm-6 col-md-4 col-lg-3">
      <!-- Content -->
    </div>
  </div>
</div>
```

In this example:

- On extra small screens (<576px): columns stack vertically (full width)
- On small screens (≥576px): 2 columns per row (6/12)
- On medium screens (≥768px): 3 columns per row (4/12)
- On large screens (≥992px): 4 columns per row (3/12)
