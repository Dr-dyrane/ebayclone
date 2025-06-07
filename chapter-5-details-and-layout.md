# Chapter 5: Details and Layout with CSS Grid 📐

Welcome to Chapter 5! This is a pivotal moment. We have our two main content blocks—the gallery and the info—but they are stacked vertically. Now, we will use **CSS Grid** to create a sophisticated, two-column layout that places them side-by-side, just like on a real e-commerce site.

### Your Mission:

**Step 1: Add the Final Detail Sections to your HTML**

First, let's add the last few pieces of information to the `product-info` section. Add this code **inside the `.product-info` div**, right after the closing `</div>` of the `.action-buttons`.

```html
      <!-- Add this code right after the action-buttons div -->
      <div class="detail-section">
        <div>✓ Breathe easy. Returns accepted.</div>
      </div>
      
      <div class="detail-section">
        <div class="detail-grid">
          <div class="detail-label">Returns:</div>
          <div>
            30 days returns. Buyer pays for return shipping. <a href="#">See details</a>
          </div>
        </div>
      </div>
      
      <div class="detail-section">
        <h2>Shop with confidence</h2>
        <div>
          <strong>eBay Money Back Guarantee</strong>
          <div>Get the item you ordered or your money back. <a href="#">Learn more</a></div>
        </div>
      </div>
```

**Step 2: Apply the CSS Grid Layout**

This is the key step. We will modify the `.product-container` and add styles for our new `.detail-grid`. Add these CSS rules to your `<style>` block.

```css
/* Find the existing .product-container rule and ADD these new properties to it. */
.product-container {
  display: grid; /* Activate Grid Layout! */
  grid-template-columns: 2fr 1fr; /* Create two columns. The first is twice as wide as the second. */
  gap: 30px; /* This creates a gutter between our columns and rows */

  /* The other styles like background-color, padding, etc. remain the same. */
  background-color: white;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}

/* Now, add this NEW rule for the smaller detail grids */
.detail-grid {
  display: grid;
  grid-template-columns: 1fr 2fr; /* Also a two-column grid, for the label and its text */
  gap: 10px;
  align-items: start; /* Aligns items to the top of their grid cell */
}
```

### What You Just Learned:

*   **CSS Grid vs. Flexbox:**
    *   **Flexbox** (which we used in the header) is excellent for laying things out in a single direction (either a row or a column).
    *   **CSS Grid** is designed for two-dimensional layouts—both rows AND columns. It's perfect for creating the main page structure, like a photo gallery next to a sidebar of information.
*   **Fractional Units (`fr`):** The `fr` unit is unique to CSS Grid. It represents a fraction of the available space in the grid container. By setting `grid-template-columns: 2fr 1fr;`, we are telling the browser: "Divide the available width into 3 equal parts. Give the first column 2 of those parts, and the second column 1 part." This creates a flexible 66% / 33% layout.
*   **Nested Grids:** You've placed a grid (`.detail-grid`) inside a larger grid (`.product-container`). This is a powerful, modern technique for building complex, component-based layouts.

### ✅ Chapter 5 Complete!

Save your file and refresh the browser. **This is the big reveal!** Your image gallery and product information should now be sitting perfectly side-by-side in a professional two-column layout.

**➡️ [Time to bring it to life in Chapter 6: JavaScript Magic - Interactivity](./chapter-6-javascript-magic.md)**