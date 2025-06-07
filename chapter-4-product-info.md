# Chapter 4: The Product Information 📝

With our gallery in place, it's time to add the "business" side of the page: the product's title, condition, price, and the all-important action buttons.

### Your Mission:

**Step 1: Add the Product Info HTML**

Let's add the HTML for this new section. Place this code **inside the `.product-container` div**, right after the closing `</div>` of the `.product-gallery`.

```html
    <!-- Product Info -->
    <div class="product-info">
      <h1>NEW Sealed Anita Goodesign SWEET TOOTH Mini Collection Machine Embroidery Design</h1>
      
      <div class="detail-section">
        <div class="detail-grid">
          <div class="detail-label">Condition:</div>
          <div>New</div>
        </div>
      </div>
      
      <div class="price">US $16.99</div>
      
      <div class="action-buttons">
        <button class="btn btn-primary">Buy It Now</button>
        <button class="btn btn-secondary">Add to cart</button>
        <button class="btn btn-watchlist">
          <span>♡</span> Add to Watchlist
        </button>
      </div>
      
      <div class="detail-section">
        <div class="detail-label">Shipping:</div>
        <div>
          US $5.70 USPS First Class®. <a href="#">See details</a>
        </div>
      </div>
    </div>
```

**Step 2: Add the Product Info CSS**

Now, let's style all that new content. Add this CSS to your `<style>` block.

```css
/* Product Info Styles */
.product-info h1 {
  font-size: 1.5rem;
  margin-bottom: 15px;
  line-height: 1.3;
}

.price {
  font-size: 1.8rem;
  font-weight: bold;
  margin: 15px 0;
  color: var(--ebay-green); /* Using our CSS variable for the price color! */
}

/* Action Buttons General Style */
.action-buttons {
  display: flex;
  flex-direction: column; /* We'll stack them vertically for now */
  gap: 10px;
  margin-bottom: 20px;
}

.btn {
  padding: 14px;
  border-radius: 6px;
  border: none;
  font-weight: bold;
  cursor: pointer;
  text-align: center;
  transition: all 0.2s ease;
}

/* Specific Button Styles */
.btn-primary {
  background-color: var(--ebay-blue);
  color: white;
}
.btn-primary:hover {
  background-color: #2851d9; /* A slightly darker blue for hover */
  transform: translateY(-2px); /* Lifts the button slightly on hover */
  box-shadow: 0 4px 12px rgba(54, 101, 243, 0.3); /* Adds a cool glow */
}

.btn-secondary {
  background-color: white;
  border: 2px solid var(--ebay-blue);
  color: var(--ebay-blue);
}
.btn-secondary:hover {
  background-color: var(--ebay-blue);
  color: white;
  transform: translateY(-2px);
}

.btn-watchlist {
  background-color: white;
  border: 2px solid var(--border-color);
  color: var(--text-color);
  display: flex; /* To align the heart icon and text */
  align-items: center;
  justify-content: center;
  gap: 8px;
}
.btn-watchlist:hover {
  border-color: var(--ebay-red);
  color: var(--ebay-red);
  transform: translateY(-2px);
}

/* Detail Section Styles */
.detail-section {
  border-top: 1px solid var(--border-color);
  padding: 15px 0;
}

.detail-label {
  font-weight: bold;
  color: var(--secondary-text);
}
```

### What You Just Learned:

*   **Component-Based Styling:** We created a generic `.btn` class that holds all the common styles for our buttons (padding, border-radius, font-weight). Then, we created specific modifier classes (`.btn-primary`, `.btn-secondary`) to handle the unique colors and borders. This is a very efficient and common practice.
*   **Advanced Hover Effects:** You've gone beyond simple color changes. `transform: translateY(-2px)` creates a subtle "lift" effect, and `box-shadow` adds a glow, making the UI feel much more responsive and premium.
*   **Styling for Readability:** By using `line-height` on the `h1` and `margin` on the `.price`, you are consciously adding "white space" that makes the content easier to read and less cramped.

### ✅ Chapter 4 Complete!

Save and refresh! All your product information should be visible and styled. However, it's probably sitting *underneath* the image gallery instead of next to it. We will fix that in the next chapter.

**➡️ [Let's create the final layout in Chapter 5: Details and Layout with CSS Grid](./chapter-5-details-and-layout.md)**