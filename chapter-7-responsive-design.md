# Chapter 7: Responsive Design 📱

Congratulations on making it to the final chapter! Our page looks great on a desktop, but what about a phone? Responsive design is the practice of making a website adapt to different screen sizes. We will use **Media Queries** to apply special styles only for smaller screens.

### Your Mission:

Add the following CSS code to the **very bottom of your `<style>` block**. This is a media query, and its rules will only apply when the browser window's width is 768 pixels or less.

```css
/* --- Responsive Design --- */
/* This block of CSS will only apply on screens 768px wide or smaller (tablets and phones) */
@media (max-width: 768px) {

  /* Change the main grid layout to a single column */
  .product-container {
    grid-template-columns: 1fr; /* Stack the gallery and info vertically */
    padding: 15px;
  }

  /* Make the header simpler */
  .header {
    padding: 10px 15px;
  }
  .user-nav {
    display: none; /* Hide the desktop navigation links to save space */
  }
  
  /* Make the action buttons fixed to the bottom of the screen for easy access */
  .action-buttons {
    position: fixed; /* Lifts the buttons out and sticks them to the viewport */
    bottom: 0;
    left: 0;
    right: 0; /* Stretching from left to right */
    
    background-color: white;
    padding: 15px;
    border-top: 1px solid var(--border-color);
    box-shadow: 0 -2px 10px rgba(0,0,0,0.1); /* Shadow at the top */
    z-index: 1100; /* Ensure it's on top of other content */
    
    flex-direction: row; /* On mobile, let's put the buttons side-by-side */
  }

  /* We need to add space at the bottom of the page so the fixed buttons don't cover content */
  .container {
    padding-bottom: 120px; 
  }

  /* Make the title and price slightly smaller on mobile */
  .product-info h1 {
    font-size: 1.3rem;
  }
  .price {
    font-size: 1.5rem;
  }

}
```

### What You Just Learned:

*   **Media Queries:** The `@media (max-width: 768px) { ... }` block is the heart of responsive design. It allows you to define CSS rules that only apply under certain conditions—in this case, when the viewport (the visible part of the browser window) is 768px or narrower.
*   **Mobile-First vs. Desktop-First:** We used a "desktop-first" approach, where we built the desktop layout and then added a media query to adjust it for mobile. The other common approach is "mobile-first," where you build for mobile and use `min-width` media queries to add complexity for larger screens. Both are valid.
*   **The "Fixed" Position:** `position: fixed` is a powerful positioning value. It attaches an element to the viewport itself, so it doesn't scroll with the page. This is perfect for creating "sticky" headers or footers, like the action buttons on many mobile apps.
*   **Content Overlap Problem:** A common "gotcha" with fixed positioning is that the fixed element can cover up content at the bottom of the page. We solved this by adding `padding-bottom` to the `.container`, creating empty space for the fixed buttons to sit over.

### ✅🎉 PROJECT COMPLETE! 🎉✅

**Congratulations!** Save your file and open it in your browser. Resize the window from wide to narrow. You will see your layout gracefully transform, adapting perfectly to the screen size.

You have successfully built a complex, interactive, and fully responsive webpage from scratch. You've tackled some of the most important concepts in modern front-end web development. Give yourself a huge pat on the back!

**You can view the final, complete code here: [final-code.html](./ebayclone.html)**