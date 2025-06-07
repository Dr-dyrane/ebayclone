# Chapter 2: The Header and Search Bar 🔍

In this chapter, we will build the entire header component. This is a complex piece involving a logo, navigation links, and a search bar. We'll use HTML for the structure and CSS with **Flexbox** to align everything perfectly.

### Your Mission:

**Step 1: Add the Header HTML**

First, let's add the HTML structure for the header. Place this code **inside your `<body>` tags**.

```html
<!-- Header -->
<header class="header">
  <div class="top-nav">
    <div class="logo">
      <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/1b/EBay_logo.svg/2560px-EBay_logo.svg.png" alt="eBay Logo">
    </div>
    <div class="user-nav" id="userNav">
      <a href="#">Hi Dyrane!</a>
      <a href="#">Daily Deals</a>
      <a href="#">Help & Contact</a>
      <a href="#">Sell</a>
      <a href="#">Watchlist</a>
      <a href="#">My eBay</a>
      <a href="#">🛒</a>
    </div>
  </div>
  <div class="search-container">
    <input type="text" placeholder="Search for anything">
    <select class="category-select">
      <option>All Categories</option>
    </select>
    <button>Search</button>
  </div>
</header>
```

**Step 2: Add the Header CSS**

Now, let's add the CSS to style our header. Place this code **inside your `<style>` tags**, below the code you added in Chapter 1.

```css
/* Header Styles */
.header {
  background-color: white;
  border-bottom: 1px solid var(--border-color);
  padding: 10px 20px;
  position: sticky; /* This makes the header stick to the top when you scroll! */
  top: 0;
  z-index: 1000; /* Ensures the header stays on top of other content */
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.top-nav {
  display: flex; /* Activate Flexbox! */
  justify-content: space-between; /* Pushes logo and nav to opposite ends */
  align-items: center; /* Vertically aligns them in the middle */
  margin-bottom: 10px;
}

.logo img {
  height: 40px; /* Control the size of the logo */
}

.user-nav {
  display: flex;
  gap: 15px; /* Adds space between each navigation link */
  font-size: 0.8rem;
}

.search-container {
  display: flex; /* Use Flexbox for the search bar too! */
  margin: 10px 0;
}

.search-container input {
  flex-grow: 1; /* Makes the input field take up all available space */
  padding: 12px;
  border: 2px solid var(--ebay-blue);
  border-right: none;
  border-radius: 4px 0 0 4px; /* Rounds only the left corners */
  font-size: 16px;
  outline: none; /* Removes the default blue outline on focus */
}

.search-container button {
  background-color: var(--ebay-blue);
  color: white;
  border: none;
  padding: 0 20px;
  border-radius: 0 4px 4px 0; /* Rounds only the right corners */
  cursor: pointer;
  font-weight: bold;
}

.category-select {
  padding: 12px;
  border: 2px solid var(--ebay-blue);
  border-left: none; /* Remove the left border to merge with the input */
  background-color: white;
  cursor: pointer;
}
```

### What You Just Learned:

*   **Semantic HTML:** We used `<header>` which tells the browser and developers that this is the introductory content for the page.
*   **Flexbox for Layout:** `display: flex` is a modern CSS tool for aligning items.
    *   `justify-content: space-between` is perfect for pushing two items to the far ends of a container.
    *   `align-items: center` centers items along the cross-axis (vertically, in this case).
    *   `gap` is a modern property to easily add space between flex items.
*   **Sticky Positioning:** `position: sticky` and `top: 0` is a powerful combination that makes an element (like our header) scroll with the page until it hits the top, at which point it "sticks" there.
*   **Form Styling:** You learned how to style form elements like `<input>`, `<select>`, and `<button>` to look like a cohesive unit, including removing borders and adjusting `border-radius` to merge them together visually.

### ✅ Chapter 2 Complete!

Save your file and refresh the browser. You should now have a fully styled, professional-looking header that sticks to the top of the page as you scroll!

**➡️ [Next up, let's build the star of the show in Chapter 3: The Product Gallery](./chapter-3-product-gallery.md)**