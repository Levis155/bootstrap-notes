# Components

Bootstrap components are pre-styled, reusable UI elements that help you quickly build functional and visually consistent interfaces without writing much CSS.

They are built using HTML + Bootstrap classes and sometimes require JavaScript for interactivity.

They can be grouped into categories: 

- **Basic content & Layout Components (alerts, badges, cards, etc.)**
- **Navigation Components (Navbar, breadcrumb, pagination, etc.)**
- **Form Components (form controls, input groups, validation)**
- **Interactive Components (modals, dropdowns, carousels, etc.)**


## Alerts

These show contextual feedback messages (success, error, warning, info).

**Features:**

- Contextual classes: alert-primary, alert-success, alert-danger, etc.
- Can be dismissible with JS support.

**Example:**

```html
<div class="alert alert-success" role="alert">
  Operation completed successfully!
</div>

<div class="alert alert-warning alert-dismissible fade show" role="alert">
  Warning! Check your inputs.
  <button type="button" class="btn-close" data-bs-dismiss="alert" aria-label="Close"></button>
</div>

```

## Badges

These are small count or label indicators.

**Features:**

- Inline text indicators for notifications or statuses. 
- Use with headings, buttons, or nav items.

**Example:**

```html
<h1>Messages <span class="badge bg-secondary">4</span></h1>
<button class="btn btn-primary">
  Notifications <span class="badge bg-light text-dark">3</span>
</button>

```

## Breadcrumb

These indicate the current page's location in navigation hierarchy.

**Example:**

```html
<nav aria-label="breadcrumb">
  <ol class="breadcrumb">
    <li class="breadcrumb-item"><a href="#">Home</a></li>
    <li class="breadcrumb-item"><a href="#">Library</a></li>
    <li class="breadcrumb-item active" aria-current="page">Data</li>
  </ol>
</nav>

```

## Buttons

**Features:**

- **Styles:** btn-primary, btn-secondary, btn-success, etc.
- **Sizes:** btn-lg, btn-sm
- **States:** disabled, active

**Example:**

```html
<button class="btn btn-primary">Primary</button>
<button class="btn btn-outline-success">Outline</button>

```

## Button Group

These group multiple buttons.

**Example:**

```html
<div class="btn-group" role="group">
  <button class="btn btn-secondary">Left</button>
  <button class="btn btn-secondary">Middle</button>
  <button class="btn btn-secondary">Right</button>
</div>

```

## Cards

These are flexible container for content  (text, images, lists, links).

**Features:**

- Header, footer, body sections
- Support for images, list groups

**Example:**

```html
<div class="card" style="width: 18rem;">
  <img src="image.jpg" class="card-img-top" alt="...">
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <p class="card-text">Short description.</p>
    <a href="#" class="btn btn-primary">Read more</a>
  </div>
</div>

```

## Carousel

These provide a means for sliding through images or content.

**Example:**

```html
<div id="carouselExample" class="carousel slide" data-bs-ride="carousel">
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img src="slide1.jpg" class="d-block w-100" alt="Slide 1">
    </div>
    <div class="carousel-item">
      <img src="slide2.jpg" class="d-block w-100" alt="Slide 2">
    </div>
  </div>
  <button class="carousel-control-prev" data-bs-target="#carouselExample" data-bs-slide="prev">
    <span class="carousel-control-prev-icon"></span>
  </button>
  <button class="carousel-control-next" data-bs-target="#carouselExample" data-bs-slide="next">
    <span class="carousel-control-next-icon"></span>
  </button>
</div>

```

## Collapse

Shows/hides content with a sliding animation.

**Example:**

```html
<p>
  <a class="btn btn-primary" data-bs-toggle="collapse" href="#collapseExample">
    Toggle
  </a>
</p>
<div class="collapse" id="collapseExample">
  <div class="card card-body">
    Hidden content here.
  </div>
</div>

```

## Dropdowns

These are toggleable menus.

**Example:**

```html
<div class="dropdown">
  <button class="btn btn-secondary dropdown-toggle" data-bs-toggle="dropdown">
    Dropdown
  </button>
  <ul class="dropdown-menu">
    <li><a class="dropdown-item" href="#">Action</a></li>
    <li><a class="dropdown-item" href="#">Another action</a></li>
  </ul>
</div>

```

## List Group

Displays a series of items.

**Example:**

```html
<ul class="list-group">
  <li class="list-group-item active">Active item</li>
  <li class="list-group-item">Item 2</li>
</ul>

```

## Modal

These facilitate popup dialog.

**Example:**

```html
<button class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#exampleModal">
  Launch modal
</button>

<div class="modal fade" id="exampleModal" tabindex="-1">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h5>Modal title</h5>
        <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
      </div>
      <div class="modal-body">Modal content...</div>
      <div class="modal-footer">
        <button class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
      </div>
    </div>
  </div>
</div>

```

## Navbar

These are responsive site navigation headers.

**Example:**

```html
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <a class="navbar-brand" href="#">Brand</a>
  <button class="navbar-toggler" data-bs-toggle="collapse" data-bs-target="#navbarNav">
    <span class="navbar-toggler-icon"></span>
  </button>
  <div class="collapse navbar-collapse" id="navbarNav">
    <ul class="navbar-nav">
      <li class="nav-item"><a class="nav-link" href="#">Home</a></li>
    </ul>
  </div>
</nav>

```

## Pagination

These offer a means for navigating between pages.

**Example:**

```html
<nav>
  <ul class="pagination">
    <li class="page-item disabled"><a class="page-link">Previous</a></li>
    <li class="page-item active"><a class="page-link">1</a></li>
    <li class="page-item"><a class="page-link">2</a></li>
    <li class="page-item"><a class="page-link">Next</a></li>
  </ul>
</nav>

```

## Progress

Show task completion status.

**Example:**

```html
<div class="progress">
  <div class="progress-bar" style="width: 50%">50%</div>
</div>

```

## Spinners

Show loading state.

**Example:**

```html
<div class="spinner-border text-primary" role="status"></div>

```