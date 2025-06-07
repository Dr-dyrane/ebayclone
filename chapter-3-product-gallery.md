# Chapter 3: The Product Gallery 🖼️

Welcome to Chapter 3! Now we'll build the most important visual part of the page: the product gallery. This will include a large main image and a set of smaller, clickable thumbnails underneath it.

### Your Mission:

**Step 1: Add the Gallery HTML**

We need a main container to hold our page content. Then, inside it, we'll build the product gallery. Add this HTML code **inside your `<body>`**, right after the closing `</header>` tag.

```html
<!-- Main Content -->
<div class="container">
  <div class="product-container">
    
    <!-- Product Gallery -->
    <div class="product-gallery">
      <div class="image-counter">102 VIEWED IN THE LAST 24 HOURS</div>
      <img class="main-image" src="https://i.ebayimg.com/images/g/NPQAAOSw2LRkUvH6/s-l1600.jpg" alt="NEW Sealed Anita Goodesign SWEET TOOTH Mini Collection Machine Embroidery Design">
      <div class="thumbnails">
        <img class="thumbnail" src="https://i.ebayimg.com/images/g/NPQAAOSw2LRkUvH6/s-l64.jpg" alt="Thumbnail 1">
        <img class="thumbnail" src="https://i.ebayimg.com/images/g/XaYAAOSwYplkUvH6/s-l64.jpg" alt="Thumbnail 2">
        <img class="thumbnail" src="https://i.ebayimg.com/images/g/qloAAOSw8dZkUvH6/s-l64.jpg" alt="Thumbnail 3">
        <img class="thumbnail" src="https://i.ebayimg.com/images/g/ZtEAAOSwEzJkUvH6/s-l64.jpg" alt="Thumbnail 4">
        <img class="thumbnail" src="https://i.ebayimg.com/images/g/TmQAAOSwnx1kUvH6/s-l64.jpg" alt="Thumbnail 5">
      </div>
    </div>
    
    <!-- We will add the product-info section here in the next chapter -->

  </div>
</div>
```

**Step 2: Add the Gallery CSS**

Now, let's style our new HTML. Add this CSS code **inside your `<style>` tags**.

```css
/* Main Content Container Styles */
.container {
  max-width: 1200px; /* Sets a maximum width for our content */
  margin: 0 auto; /* A classic trick to center a block element */
  padding: 20px;
}

.product-container {
  background-color: white;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}

/* Product Gallery Styles */
.product-gallery {
  position: relative; /* This is crucial for positioning the image counter */
}

.main-image {
  width: 100%; /* Makes the image take the full width of its container */
  height: auto; /* Maintains the aspect ratio */
  border: 1px solid var(--border-color);
  border-radius: 8px;
  cursor: zoom-in; /* Indicates to the user that the image is clickable */
}

/* Thumbnail Styles */
.thumbnails {
  display: flex; /* We use flexbox again to line up the thumbnails */
  overflow-x: auto; /* If there are too many thumbnails, they become scrollable */
  gap: 8px;
  margin-top: 15px;
  padding: 10px 0;
}

.thumbnail {
  min-width: 70px; /* Ensures thumbnails don't get too small */
  width: 70px;
  height: 70px;
  border: 2px solid var(--border-color);
  cursor: pointer;
  border-radius: 6px;
  object-fit: cover; /* Prevents the images from being squished */
  transition: all 0.2s ease; /* Adds a smooth effect for hover */
}

.thumbnail:hover {
  border-color: var(--ebay-blue); /* Highlight on hover */
}

/* Image Counter Styles */
.image-counter {
  position: absolute; /* Positions this element relative to .product-gallery */
  top: 15px;
  left: 15px;
  background-color: var(--ebay-red);
  color: white;
  padding: 6px 12px;
  border-radius: 20px;
  font-size: 0.75rem;
  font-weight: bold;
}
```

### What You Just Learned:

*   **Containing Layouts:** The `.container` class is a standard web development practice. It gives your main content a maximum width and centers it, which looks much better on wide screens than a full-width layout.
*   **Relative & Absolute Positioning:**
    *   We set `.product-gallery` to `position: relative`. This doesn't change its position, but it creates a "positioning context" for its children.
    *   We then set `.image-counter` to `position: absolute`. This lifts it out of the normal document flow and allows us to position it precisely (`top: 15px`, `left: 15px`) *relative to its parent*, `.product-gallery`.
*   **Horizontal Scrolling with Flexbox:** By setting `overflow-x: auto` on a flex container (`.thumbnails`), you create a horizontally scrollable list. This is a very common pattern for mobile-friendly galleries.
*   **`object-fit: cover`:** This CSS property is incredibly useful for images. It tells the image to fill its container's dimensions while maintaining its aspect ratio, cropping any excess. This prevents images from looking stretched or squished.

### ✅ Chapter 3 Complete!

Save and refresh your page. You now have a beautiful, functional-looking image gallery. The thumbnails don't *do* anything yet, but the visual structure is complete.

**➡️ [Time to add the text in Chapter 4: The Product Information](./chapter-4-product-info.md)**