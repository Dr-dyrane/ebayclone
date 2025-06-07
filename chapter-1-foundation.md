# Chapter 1: The Foundation 🏗️

Welcome to the first step! In this chapter, we'll set up the basic HTML document structure and add the initial, foundational CSS that will define our project's look and feel. This includes a "CSS Reset" and defining our color palette with CSS Variables.

### Your Mission:

Copy the code below and paste it into your empty `ebay-clone.html` file.

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>
			NEW Sealed Anita Goodesign SWEET TOOTH Mini Collection Machine Embroidery
			Design | eBay
		</title>
		<style>
			/* 
      First, we define our color palette using CSS Variables.
      This lets us reuse colors easily without having to remember the hex codes.
      We define them inside :root so they are available globally.
    */
			:root {
				--ebay-blue: #3665f3;
				--ebay-red: #e53238;
				--ebay-yellow: #f5af02;
				--ebay-green: #86b817;
				--light-gray: #f7f7f7;
				--border-color: #e5e5e5;
				--text-color: #333;
				--secondary-text: #707070;
			}

			/* 
      Next, a CSS Reset. Browsers have default margins and paddings that
      can make our layout inconsistent. This removes them all.
      The * is a "wildcard" selector that targets every single element.
    */
			* {
				margin: 0;
				padding: 0;
				box-sizing: border-box;
				font-family: "Helvetica", "Arial", sans-serif;
			}

			/* Finally, some base styles for the entire page */
			body {
				background-color: var(--light-gray); /* We use our variable here! */
				color: var(--text-color);
				line-height: 1.5;
				overflow-x: hidden; /* Prevents accidental horizontal scrolling */
			}

			a {
				text-decoration: none;
				color: #0654ba;
			}
		</style>
	</head>
	<body>
		<!-- Our page content will go here in the next chapters! -->
	</body>
</html>
```

### What You Just Built:

1.  **HTML Boilerplate:** The essential `<!DOCTYPE>`, `<html>`, `<head>`, and `<body>` tags.
2.  **Meta Tags:** The `<meta>` tags are crucial. `charset="UTF-8"` ensures all text and symbols display correctly. `name="viewport"` is **essential for responsive design**, telling mobile browsers to render the page at the device's actual width.
3.  **CSS Variables:** Inside `:root`, we've created reusable variables for all of eBay's brand colors. Now, instead of typing `#3665f3`, we can just type `var(--ebay-blue)`. This makes our code cleaner and easier to update.
4.  **CSS Reset:** The `* { ... }` block is a professional technique to ensure our website looks the same across all browsers (Chrome, Firefox, Safari) by removing their default styling. `box-sizing: border-box` is a critical rule that makes layout math much more intuitive.

### ✅ Chapter 1 Complete!

You've laid a professional-grade foundation. If you open the file now, you'll just see a blank gray page, but you've set the stage perfectly for what's to come.

**➡️ [Let's build the top of our page in Chapter 2: The Header and Search Bar](./chapter-2-header-and-search.md)**
