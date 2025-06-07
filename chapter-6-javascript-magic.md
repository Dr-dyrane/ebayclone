# Chapter 6: JavaScript Magic - Interactivity ⚙️

Welcome to the magic show! Our page looks fantastic, but it's static. In this chapter, we'll write JavaScript to make our page respond to user actions. We will make the thumbnails clickable, and we'll add interactivity to the "Add to Watchlist" button.

### Your Mission:

**Step 1: Add the `<script>` Tag**

First, we need a place for our magic spells. Add opening and closing `<script>` tags at the **very bottom of your `<body>` section**, just before the closing `</body>` tag. All our JavaScript will go inside here.

```html
  ...
  </div> <!-- This is the closing div for .container -->
  
  <script>
    // Our JavaScript magic will go here!
  </script>

</body>
```

**Step 2: Make the Thumbnails Work**

Copy this JavaScript code and place it **inside your new `<script>` tags**.

```javascript
// --- Thumbnail Image Switcher ---

// 1. Find all the elements we need to work with.
const mainImage = document.querySelector('.main-image');
const thumbnails = document.querySelectorAll('.thumbnail');

// 2. Add an event listener to each thumbnail.
thumbnails.forEach(thumb => {
  thumb.addEventListener('click', function() {
    // 3. When a thumbnail is clicked, run this code.
    
    // Get the small image 'src' and make it point to the big version.
    // The image URLs on eBay often use 's-l64' for thumbnails and 's-l1600' for large images.
    const newImageSrc = thumb.src.replace('s-l64', 's-l1600');
    
    // Set the main image's src to our new, big image URL.
    mainImage.src = newImageSrc;
  });
});
```

**Step 3: Make the Watchlist Button Work**

Next, let's add a trick for the watchlist button. Add this code **inside your `<script>` tags**, right below the thumbnail code.

```javascript
// --- Watchlist Button Toggle ---

// 1. Find the watchlist button.
const watchlistBtn = document.querySelector('.btn-watchlist');
const watchlistIcon = watchlistBtn.querySelector('span'); // Find the heart icon inside the button

// 2. Add a click listener to the button.
watchlistBtn.addEventListener('click', function() {
  // 3. Check if the button is already "active".
  // The 'contains' method checks if an element has a certain CSS class.
  const isActive = watchlistBtn.classList.contains('active');

  if (isActive) {
    // If it IS active, remove the active class.
    watchlistBtn.classList.remove('active');
    watchlistIcon.textContent = '♡'; // Change heart back to outline
    alert('Item removed from your watchlist!');
  } else {
    // If it IS NOT active, add the active class.
    watchlistBtn.classList.add('active');
    watchlistIcon.textContent = '❤️'; // Change heart to solid red
    alert('Item added to your watchlist!');
  }
});
```

**Step 4: Add CSS for the "Active" Watchlist State**

Our JavaScript adds an `.active` class to the button, but we haven't told the CSS what that class should *do*. Add this final piece of CSS to your `<style>` block.

```css
/* Style for when the watchlist button is active */
.btn-watchlist.active {
  background-color: var(--ebay-red);
  border-color: var(--ebay-red);
  color: white;
}
```

### What You Just Learned:

*   **The DOM (Document Object Model):** JavaScript sees your HTML page as a "Document Object". We use commands like `document.querySelector` to find and grab specific elements from this document.
*   **Event Listeners:** `addEventListener` is the cornerstone of interactive JavaScript. It tells the browser to "listen" for a specific event (like a `'click'`) on an element and then execute a function (the "callback function") when that event happens.
*   **Manipulating Elements:** You learned how to change things on the page with JavaScript:
    *   `mainImage.src = ...` changes an image's source.
    *   `watchlistIcon.textContent = ...` changes the text inside an element.
    *   `watchlistBtn.classList.add/remove(...)` adds or removes a CSS class, allowing you to dynamically change an element's styling.
*   **State Management with Classes:** Using a CSS class like `.active` to represent the "state" of a button is a clean and powerful pattern. The JavaScript handles the logic, and the CSS handles the visual representation of that state.

### ✅ Chapter 6 Complete!

Save and refresh! Your page is now interactive. Click the thumbnails to change the main image. Click the watchlist button to see it toggle its state and show an alert.

**➡️ [Let's make it perfect on all devices in our final chapter: Chapter 7 - Responsive Design](./chapter-7-responsive-design.md)**