# Media Object

The media object in Bootstrap is a flexible component for building layouts where you have media content (like images or icons) placed alongside textual content.

- It’s often used for comments sections, list items with thumbnails, chat messages, or articles with author photos. 
- It uses flexbox utilities internally for alignment.

## Structure of the Media Object

The basic structure looks like this:

```html
<div class="media">
  <img src="..." class="mr-3" alt="...">
  <div class="media-body">
    <h5 class="mt-0">Heading</h5>
    Text content here...
  </div>
</div>

```

**Parts:**

1. **.media** → The main wrapper. 
2. **Media element** → Typically an image, svg, or video placed to the left or right. 
3. **.media-body** → Flexible content container that takes the remaining horizontal space. 
4. **Alignment classes** → Spacing/margins (mr-*, ml-*) and vertical alignment (align-self-start, etc.).

The following is an example of a basic left-aligned media object:

```html
<div class="media">
  <img src="user.jpg" class="mr-3" alt="User avatar" width="64">
  <div class="media-body">
    <h5 class="mt-0">John Doe</h5>
    This is an example of a Bootstrap media object where an image sits next to text.
  </div>
</div>

```

How it works:
- The image is given a right margin (mr-3) to separate it from the text. 
- The .media-body expands to fill the remaining space.

The following is an example of a right-aligned media object:

```html
<div class="media">
  <div class="media-body">
    <h5 class="mt-0">Message Title</h5>
    Content goes here...
  </div>
  <img src="icon.png" class="ml-3" alt="Icon" width="64">
</div>

```

## Nesting Media objects

You can nest another .media inside .media-body to create threaded discussions.

```html
<div class="media">
  <img src="user1.jpg" class="mr-3" alt="User1" width="64">
  <div class="media-body">
    <h5 class="mt-0">Parent Comment</h5>
    This is the first comment.

    <div class="media mt-3">
      <img src="user2.jpg" class="mr-3" alt="User2" width="64">
      <div class="media-body">
        <h5 class="mt-0">Reply</h5>
        This is a reply inside another media object.
      </div>
    </div>
  </div>
</div>

```

This creates a comment with a nested reply layout.

## Alignment in Media Objects

Since the media object is flexbox-based, you can use vertical alignment utilities:

```html
<div class="media">
  <img src="photo.jpg" class="align-self-start mr-3" alt="..." width="64">
  <div class="media-body">
    Top aligned content
  </div>
</div>

<div class="media">
  <img src="photo.jpg" class="align-self-center mr-3" alt="..." width="64">
  <div class="media-body">
    Center aligned content
  </div>
</div>

<div class="media">
  <img src="photo.jpg" class="align-self-end mr-3" alt="..." width="64">
  <div class="media-body">
    Bottom aligned content
  </div>
</div>

```

## Spacing and Utilities

Common spacing classes you might use:

- **Horizontal margin:** mr-* (right margin) or ml-* (left margin)
- **Vertical margin:** mt-*, mb-*
- **Responsive spacing:** e.g., mr-md-4 (only from medium screens up)

## Media Lists

Media objects can be placed inside list groups to display multiple entries (like chat messages or articles list).

```html
<ul class="list-unstyled">
  <li class="media">
    <img src="thumb1.jpg" class="mr-3" alt="Thumb" width="64">
    <div class="media-body">
      <h5 class="mt-0 mb-1">List Item 1</h5>
      Content for the first item.
    </div>
  </li>
  <li class="media my-4">
    <img src="thumb2.jpg" class="mr-3" alt="Thumb" width="64">
    <div class="media-body">
      <h5 class="mt-0 mb-1">List Item 2</h5>
      Content for the second item.
    </div>
  </li>
</ul>

```

## Bootstrap 5 Note

In Bootstrap 5, the .media component was removed in favor of using utility classes with flexbox. You can replicate the same layout with:

```html
<div class="d-flex">
  <div class="flex-shrink-0">
    <img src="..." alt="..." width="64">
  </div>
  <div class="flex-grow-1 ms-3">
    Content goes here
  </div>
</div>

```

This works exactly like .media but uses d-flex, flex-shrink-0, flex-grow-1, and margin spacing.