# 🎨 Building Your Very Own eBay Website - A Fun Adventure!

_A Step-by-Step Guide for Young Web Developers_

---

## 📚 Table of Contents

1.  [What We're Building](#what-were-building)
2.  [Getting Ready](#getting-ready)
3.  [Chapter 1: HTML - Building Blocks 🧱](#chapter-1-html---building-blocks)
4.  [Chapter 2: CSS - Making It Pretty 🎨](#chapter-2-css---making-it-pretty)
5.  [Chapter 3: JavaScript - Making It Move 🎮](#chapter-3-javascript---making-it-move)
6.  [Chapter 4: Making It Work on Phones 📱](#chapter-4-making-it-work-on-phones)
7.  [Chapter 5: Adding Cool Effects ✨](#chapter-5-adding-cool-effects)
8.  [Final Project 🎯](#final-project)

---

## 🎯 What We're Building

Imagine you're building a LEGO house, but instead of plastic bricks, we're using computer code! We're going to build a website that looks just like an eBay product page—a place where people buy and sell things online.

**What our website will have:**

- 📸 Pictures of products you can click on
- 🛒 Buttons to "Buy" and "Add to Cart"
- 💰 Prices and product information
- 📱 A design that works on phones and computers
- ✨ Cool animations and effects

---

## 🛠️ Getting Ready

Before we start building, let's get our tools ready!

### What You Need:

1.  **A Computer** (like having a workbench)
2.  **A Text Editor** (like Notepad, TextEdit, or VS Code - this is where we write our code)
3.  **A Web Browser** (like Chrome, Firefox, or Safari - this shows us our website)

### Creating Our First File:

1.  Open your text editor.
2.  Create a new file and save it as `my-ebay-clone.html`. Make sure it's saved as `.html` and not `.txt`.
3.  This will be our main building file!

---

# Chapter 1: HTML - Building Blocks

Think of HTML like the skeleton of our website—it gives structure to everything!

## Step 1: The Basic Structure

Let's start with the most basic HTML structure. Copy this into your `my-ebay-clone.html` file:

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>My eBay Clone</title>
	</head>
	<body>
		<h1>Welcome to My eBay Clone!</h1>
	</body>
</html>
```

**What does this mean?**

- `<!DOCTYPE html>` - Tells the computer "Hey, this is a website!"
- `<html>` - This is like the big box that holds everything.
- `<head>` - This is like the brain; it has information about our website that you don't see on the page.
- `<title>` - This is what shows up in the browser tab.
- `<body>` - This is where all the visible stuff goes (text, images, buttons).
- `<h1>` - This makes big, bold text (like a title).

**🎮 Try it:** Save your file and open it in a web browser. You should see "Welcome to My eBay Clone!" in big letters!

## Step 2: Adding the Header

Now let's add the top part of our website, like where eBay's logo and search bar go. Replace the `<h1>...</h1>` line with this:

```html
<body>
	<!-- This is the top part of our website -->
	<header>
		<div class="top-nav">
			<div class="logo">
				<h2>eBay Clone</h2>
			</div>
			<div class="user-links">
				<a href="#">Hi Friend!</a>
				<a href="#">Daily Deals</a>
				<a href="#">Sell</a>
				<a href="#">My eBay</a>
			</div>
		</div>

		<div class="search-area">
			<input type="text" placeholder="Search for anything" />
			<button>Search</button>
		</div>
	</header>
</body>
```

**What's new here?**

- `<header>` - A box for the top section of our website.
- `<div>` - Like invisible boxes that group things together.
- `class="..."` - Like giving names to our boxes so we can style them later with CSS.
- `<a href="#">` - These are links. The `#` means they don't go anywhere yet.
- `<input>` - A text box where people can type.
- `<button>` - A clickable button.

## Step 3: Adding the Main Product Area

Now let's add the main part where we show the product. Add this code right after the `</header>` tag.

```html
<!-- Add this after the header -->
<main class="container">
	<div class="product-section">
		<!-- Left side - Product Images -->
		<div class="product-gallery">
			<img
				class="main-image"
				src="https://via.placeholder.com/400x300/4CAF50/white?text=Cool+Toy+Robot"
				alt="Product Image"
			/>
			<div class="thumbnails">
				<img
					class="thumbnail"
					src="https://via.placeholder.com/60x60/4CAF50/white?text=1"
					alt="Thumbnail 1"
				/>
				<img
					class="thumbnail"
					src="https://via.placeholder.com/60x60/2196F3/white?text=2"
					alt="Thumbnail 2"
				/>
				<img
					class="thumbnail"
					src="https://via.placeholder.com/60x60/FF9800/white?text=3"
					alt="Thumbnail 3"
				/>
			</div>
		</div>

		<!-- Right side - Product Information -->
		<div class="product-info">
			<h1>Cool Toy Robot</h1>
			<div class="seller-info">
				<p><strong>Seller:</strong> Awesome Toy Store</p>
				<p>99.5% positive feedback</p>
			</div>
			<div class="price">$19.99</div>
			<div class="buttons">
				<button class="buy-now-btn">Buy It Now</button>
				<button class="add-cart-btn">Add to Cart</button>
				<button class="watchlist-btn">Add to Watchlist</button>
			</div>
		</div>
	</div>
</main>
```

**What's happening here?**

- `<main>` - The main content area of the page.
- `<img>` - This tag shows pictures! The `src` tells it where to find the picture.
- `alt` - This describes the picture for people who can't see it.
- We're using placeholder images from a website (`via.placeholder.com`) so we don't have to download any pictures. They're just gray boxes with text for now!

## Step 4: Adding Similar Items

Let's add a section that shows other products you might like. Add this code inside the `<main>` tag, right after the `product-section`'s closing `</div>`.

```html
<!-- Add this after the product-section div -->
<section class="similar-items">
	<h2>Similar Items</h2>
	<div class="items-grid">
		<div class="item-card">
			<img
				src="https://via.placeholder.com/150x150/9C27B0/white?text=Toy+1"
				alt="Similar Item 1"
			/>
			<h3>Another Cool Toy</h3>
			<p class="item-price">$15.99</p>
		</div>
		<div class="item-card">
			<img
				src="https://via.placeholder.com/150x150/3F51B5/white?text=Game"
				alt="Similar Item 2"
			/>
			<h3>Super Fun Game</h3>
			<p class="item-price">$24.99</p>
		</div>
		<div class="item-card">
			<img
				src="https://via.placeholder.com/150x150/009688/white?text=Puzzle"
				alt="Similar Item 3"
			/>
			<h3>Amazing Puzzle</h3>
			<p class="item-price">$12.99</p>
		</div>
	</div>
</section>
```

## Step 5: Adding a Footer

Every website needs a bottom part to finish it off. Add this code right before the closing `</body>` tag.

```html
<!-- Add this before </body> -->
<footer>
	<p>&copy; 2024 My eBay Clone. Made with ❤️</p>
</footer>
```

**🎮 Try it:** Save your file and refresh your browser. You should see a basic website structure with a header, a product area, similar items, and a footer. It's messy, but all the parts are there!

---

# Chapter 2: CSS - Making It Pretty

Our website looks very plain—like a coloring book before you add colors! CSS (Cascading Style Sheets) is what we'll use to make it beautiful.

## Step 1: Adding CSS to Our HTML

First, we need a place to write our CSS code. Add a `<style>` tag inside the `<head>` section of your HTML file.

```html
<head>
	<meta charset="UTF-8" />
	<meta name="viewport" content="width=device-width, initial-scale=1.0" />
	<title>My eBay Clone</title>
	<style>
		/* Our CSS will go here! */
	</style>
</head>
```

## Step 2: Basic Styling

Let's start with some basic colors and fonts to make the whole page look nicer. Add this code inside your new `<style>` tag.

```css
/* Reset - This makes all browsers show our site the same way */
* {
	margin: 0;
	padding: 0;
	box-sizing: border-box;
}

/* Make the whole page look nice */
body {
	font-family: Arial, sans-serif;
	background-color: #f7f7f7; /* A light gray background */
	color: #333; /* Dark gray text */
}

/* Style the header */
header {
	background-color: white;
	border-bottom: 1px solid #e5e5e5;
	padding: 10px 20px;
}

.top-nav {
	display: flex; /* Lines up items in a row */
	justify-content: space-between; /* Puts space between the logo and links */
	align-items: center; /* Vertically aligns them in the middle */
	margin-bottom: 10px;
}

.logo h2 {
	color: #e53238; /* eBay's red color */
	font-size: 24px;
}

.user-links {
	display: flex;
	gap: 15px; /* Adds space between the links */
}

.user-links a {
	text-decoration: none; /* Removes the underline from links */
	color: #333;
	font-size: 14px;
}

.user-links a:hover {
	color: #0654ba; /* eBay's blue color for hover */
}
```

**What's happening here?**

- `*` - This affects EVERYTHING on the page. We use it to reset default styles.
- `body` - This styles the main body of our website.
- `.top-nav`, `.logo`, etc. - We are targeting the boxes we named with `class` in our HTML.
- `display: flex` - This is a super powerful tool for aligning items in rows or columns.
- `:hover` - This changes how something looks when you move your mouse over it.

## Step 3: Styling the Search Area

Let's make that search bar look like the real thing. Add this to your CSS.

```css
.search-area {
	display: flex;
	max-width: 600px;
	margin: 0 auto; /* Centers the search bar */
}

.search-area input {
	flex: 1; /* Makes the input box take up all available space */
	padding: 12px;
	border: 2px solid #3665f3; /* Blue border */
	border-right: none;
	border-radius: 4px 0 0 4px; /* Rounds the left corners */
	font-size: 16px;
}

.search-area button {
	background-color: #3665f3; /* Blue button */
	color: white;
	border: none;
	padding: 12px 20px;
	border-radius: 0 4px 4px 0; /* Rounds the right corners */
	cursor: pointer; /* Makes the mouse a pointer on hover */
	font-weight: bold;
}

.search-area button:hover {
	background-color: #2851d9; /* A darker blue on hover */
}
```

## Step 4: Styling the Main Product Area

Now for the main event! Let's organize the product images and info side-by-side.

```css
.container {
	max-width: 1200px;
	margin: 20px auto; /* Centers the main content */
	padding: 0 20px;
}

.product-section {
	display: grid; /* We'll create a grid layout */
	grid-template-columns: 1fr 1fr; /* Two columns of equal size */
	gap: 30px; /* Space between the columns */
	background-color: white;
	padding: 20px;
	border-radius: 8px;
	box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); /* Adds a subtle shadow */
}

.main-image {
	width: 100%;
	height: auto;
	border: 1px solid #e5e5e5;
	border-radius: 8px;
}

.thumbnails {
	display: flex;
	gap: 10px;
	margin-top: 15px;
}

.thumbnail {
	width: 60px;
	height: 60px;
	border: 2px solid #e5e5e5;
	border-radius: 4px;
	cursor: pointer;
}

.thumbnail:hover {
	border-color: #3665f3; /* Highlights the thumbnail on hover */
}
```

## Step 5: Styling Product Information and Buttons

Let's make the text and buttons look great.

```css
.product-info h1 {
	font-size: 24px;
	margin-bottom: 15px;
}

.seller-info {
	background-color: #f8f9fa;
	padding: 15px;
	border-radius: 6px;
	margin-bottom: 15px;
}

.price {
	font-size: 28px;
	font-weight: bold;
	color: #86b817; /* eBay's green color for prices */
	margin: 20px 0;
}

.buttons {
	display: flex;
	flex-direction: column; /* Stacks the buttons vertically */
	gap: 10px;
}

.buttons button {
	padding: 14px;
	border-radius: 6px;
	font-weight: bold;
	cursor: pointer;
	border: none;
	font-size: 16px;
}

.buy-now-btn {
	background-color: #3665f3;
	color: white;
}

.add-cart-btn {
	background-color: white;
	color: #3665f3;
	border: 2px solid #3665f3;
}

.watchlist-btn {
	background-color: white;
	color: #333;
	border: 2px solid #e5e5e5;
}
```

## Step 6: Styling Similar Items

Let's make the similar items look like a nice gallery.

```css
.similar-items {
	margin-top: 30px;
	background-color: white;
	padding: 20px;
	border-radius: 8px;
	box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.similar-items h2 {
	margin-bottom: 20px;
}

.items-grid {
	display: grid;
	grid-template-columns: repeat(
		auto-fit,
		minmax(150px, 1fr)
	); /* Creates as many columns as fit */
	gap: 20px;
}

.item-card {
	border: 1px solid #e5e5e5;
	border-radius: 8px;
	padding: 15px;
	text-align: center;
}

.item-card img {
	width: 100%;
	height: 120px;
	object-fit: contain; /* Makes sure the image fits without squishing */
	margin-bottom: 10px;
}

.item-card h3 {
	font-size: 16px;
	margin-bottom: 8px;
}

.item-price {
	font-size: 18px;
	font-weight: bold;
	color: #86b817;
}
```

## Step 7: Styling the Footer

Finally, let's style the footer.

```css
footer {
	text-align: center;
	padding: 20px;
	margin-top: 30px;
	color: #707070; /* A lighter gray for footer text */
}
```

**🎮 Try it:** Save your file and refresh your browser. Wow! Your website should look much more colorful and organized now!

---

# Chapter 3: JavaScript - Making It Move

JavaScript is like magic—it makes our website interactive and do things when you click!

## Step 1: Adding JavaScript to Our HTML

Add a `<script>` tag right before the closing `</body>` tag. This is where we'll write our JavaScript code.

```html
    <footer>...</footer>

    <script>
        // Our JavaScript magic will go here!
        console.log("Hello from JavaScript!");
    </script>
</body>
```

**🎮 Try it:** Open your browser's developer tools (usually by right-clicking and choosing "Inspect", then going to the "Console" tab). You should see the message "Hello from JavaScript!".

## Step 2: Making Thumbnails Clickable

Let's make it so when you click a small picture, the big picture changes. Add this code inside your `<script>` tag.

```javascript
// Find all the small thumbnail images and the main image
const thumbnails = document.querySelectorAll(".thumbnail");
const mainImage = document.querySelector(".main-image");

// Loop through each thumbnail
thumbnails.forEach(function (thumbnail) {
	// Add a click listener to each one
	thumbnail.addEventListener("click", function () {
		// When a thumbnail is clicked, change the main image's src
		// to the thumbnail's src. We'll also make it bigger.
		let newImageSrc = thumbnail.src.replace("60x60", "400x300");
		mainImage.src = newImageSrc;
	});
});
```

**What's happening here?**

- `document.querySelector` - Finds the first element that matches (like `.main-image`).
- `document.querySelectorAll` - Finds ALL elements that match (like all `.thumbnail`s).
- `addEventListener('click', ...)` - Listens for mouse clicks and runs a function when one happens.
- `mainImage.src = ...` - This changes the source of the main image, which makes a new picture appear!

## Step 3: Making Buttons Interactive

Let's make our buttons do something when clicked. For now, they'll just show a popup message.

```javascript
// Find the buttons
const buyNowBtn = document.querySelector(".buy-now-btn");
const addCartBtn = document.querySelector(".add-cart-btn");
const watchlistBtn = document.querySelector(".watchlist-btn");

// Add click listeners
buyNowBtn.addEventListener("click", function () {
	alert("🎉 Redirecting to checkout! (This is just pretend)");
});

addCartBtn.addEventListener("click", function () {
	alert("🛒 Item added to cart! (This is just pretend)");
});

// Let's make the watchlist button special
let isInWatchlist = false;
watchlistBtn.addEventListener("click", function () {
	if (isInWatchlist) {
		watchlistBtn.textContent = "Add to Watchlist";
		watchlistBtn.style.color = "#333";
		alert("💔 Removed from watchlist");
		isInWatchlist = false;
	} else {
		watchlistBtn.textContent = "In Watchlist ❤️";
		watchlistBtn.style.color = "#e53238";
		alert("❤️ Added to watchlist!");
		isInWatchlist = true;
	}
});
```

**🎮 Try it:** Save your file and refresh. Now try clicking the thumbnails and the action buttons. Your website is alive!

---

# Chapter 4: Making It Work on Phones

Lots of people use phones to look at websites. Let's make sure our site looks good on small screens! This is called **Responsive Design**.

## Step 1: Adding Mobile-Friendly CSS

We use something called a **media query** to apply styles only when the screen is smaller than a certain size. Add this CSS to the bottom of your `<style>` section.

```css
/* Mobile styles - when the screen is smaller than 768px wide */
@media (max-width: 768px) {
	/* Make the product section stack vertically on mobile */
	.product-section {
		grid-template-columns: 1fr; /* Change from 2 columns to 1 */
	}

	/* Make buttons stick to the bottom of the screen for easy access */
	.buttons {
		position: fixed; /* Stick it to the screen */
		bottom: 0;
		left: 0;
		right: 0;
		background-color: white;
		padding: 15px;
		border-top: 1px solid #e5e5e5;
		box-shadow: 0 -2px 10px rgba(0, 0, 0, 0.1);
		flex-direction: row; /* Put buttons side-by-side on mobile */
	}

	/* Add space at the bottom of the page so the buttons don't cover content */
	.container {
		padding-bottom: 100px;
	}

	/* Make similar items scroll horizontally instead of wrapping */
	.items-grid {
		display: flex; /* Change from grid to flex */
		overflow-x: auto; /* Allow horizontal scrolling */
		gap: 15px;
		padding-bottom: 10px; /* Add some space for the scrollbar */
	}

	.item-card {
		min-width: 180px; /* Give each card a fixed width */
		flex-shrink: 0; /* Stop cards from shrinking */
	}

	/* Hide some links to save space */
	.user-links a:not(:first-child) {
		display: none;
	}
}
```

**🎮 Try it:** Save and refresh. Now, make your browser window very narrow. You should see the layout change! The product image will be on top of the info, and the buttons will stick to the bottom.

---

# Chapter 5: Adding Cool Effects

Let's add some fancy animations to make our website feel more professional and fun!

## Step 1: Adding Smooth Transitions and Hover Effects

We can make style changes (like on `:hover`) happen smoothly instead of instantly. Add this CSS.

```css
/* Add this to your main button styles */
.buttons button {
	/* ... other styles ... */
	transition: all 0.3s ease; /* Makes all changes take 0.3 seconds */
}

.buy-now-btn:hover {
	background-color: #2851d9;
	transform: translateY(-2px); /* Lifts the button up slightly */
}

.add-cart-btn:hover {
	background-color: #eef2ff;
	transform: translateY(-2px);
}

.watchlist-btn:hover {
	border-color: #dcdcdc;
	transform: translateY(-2px);
}

/* Add a transition to the item cards */
.item-card {
	/* ... other styles ... */
	transition: all 0.3s ease;
}

.item-card:hover {
	transform: translateY(-4px); /* Lift the card up */
	box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1); /* Give it a bigger shadow */
}
```

## Step 2: Adding a Loading Animation

Let's make the main content fade in nicely when the page loads. We use `@keyframes` to define an animation.

```css
/* Put this at the bottom of your CSS, outside the media query */
@keyframes fadeIn {
	from {
		opacity: 0;
		transform: translateY(20px);
	}
	to {
		opacity: 1;
		transform: translateY(0);
	}
}

/* Apply the animation to the product section */
.product-section {
	/* ... other styles ... */
	animation: fadeIn 0.6s ease-out;
}

.similar-items {
	/* ... other styles ... */
	animation: fadeIn 0.8s ease-out;
}
```

## Step 3: Adding Image Zoom

Let's make the main product image zoom in when you click it. First, add the CSS for the zoom overlay.

```css
/* CSS for the zoom effect */
.main-image {
	cursor: zoom-in;
}

.image-zoom-overlay {
	position: fixed;
	top: 0;
	left: 0;
	width: 100%;
	height: 100%;
	background-color: rgba(0, 0, 0, 0.8);
	display: flex;
	align-items: center;
	justify-content: center;
	z-index: 2000; /* Makes it appear on top of everything */
	cursor: zoom-out;
}

.image-zoom-overlay img {
	max-width: 90%;
	max-height: 90%;
}
```

Now, add the JavaScript to make it work.

```javascript
// Add this to your script tag
mainImage.addEventListener("click", function () {
	// Create the black overlay
	const overlay = document.createElement("div");
	overlay.className = "image-zoom-overlay";

	// Create the image to put inside the overlay
	const zoomedImage = document.createElement("img");
	zoomedImage.src = mainImage.src;

	// Put the image in the overlay, and the overlay on the page
	overlay.appendChild(zoomedImage);
	document.body.appendChild(overlay);

	// When the overlay is clicked, remove it
	overlay.addEventListener("click", function () {
		document.body.removeChild(overlay);
	});
});
```

**🎮 Try it:** Save, refresh, and hover over the buttons and cards. Click the main product image to see it zoom!

---

# Final Project

Congratulations! You've built an amazing eBay clone! You learned how to structure a page with HTML, style it with CSS, and make it interactive with JavaScript.

Here is the complete, final code for you to check your work.

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>My eBay Clone</title>
		<style>
			/* Reset */
			* {
				margin: 0;
				padding: 0;
				box-sizing: border-box;
			}

			/* Basic Styles */
			body {
				font-family: Arial, sans-serif;
				background-color: #f7f7f7;
				color: #333;
			}

			/* Header */
			header {
				background-color: white;
				border-bottom: 1px solid #e5e5e5;
				padding: 10px 20px;
				position: sticky;
				top: 0;
				z-index: 100;
			}
			.top-nav {
				display: flex;
				justify-content: space-between;
				align-items: center;
				margin-bottom: 10px;
			}
			.logo h2 {
				color: #e53238;
				font-size: 24px;
			}
			.user-links {
				display: flex;
				gap: 15px;
			}
			.user-links a {
				text-decoration: none;
				color: #333;
				font-size: 14px;
			}
			.user-links a:hover {
				color: #0654ba;
			}
			.search-area {
				display: flex;
				max-width: 600px;
				margin: 0 auto;
			}
			.search-area input {
				flex: 1;
				padding: 12px;
				border: 2px solid #3665f3;
				border-right: none;
				border-radius: 4px 0 0 4px;
				font-size: 16px;
			}
			.search-area button {
				background-color: #3665f3;
				color: white;
				border: none;
				padding: 12px 20px;
				border-radius: 0 4px 4px 0;
				cursor: pointer;
				font-weight: bold;
			}
			.search-area button:hover {
				background-color: #2851d9;
			}

			/* Main Content */
			.container {
				max-width: 1200px;
				margin: 20px auto;
				padding: 0 20px;
			}
			.product-section {
				display: grid;
				grid-template-columns: 1fr 1fr;
				gap: 30px;
				background-color: white;
				padding: 20px;
				border-radius: 8px;
				box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
				animation: fadeIn 0.6s ease-out;
			}
			.product-gallery .main-image {
				width: 100%;
				height: auto;
				border: 1px solid #e5e5e5;
				border-radius: 8px;
				cursor: zoom-in;
			}
			.thumbnails {
				display: flex;
				gap: 10px;
				margin-top: 15px;
			}
			.thumbnail {
				width: 60px;
				height: 60px;
				border: 2px solid #e5e5e5;
				border-radius: 4px;
				cursor: pointer;
			}
			.thumbnail:hover {
				border-color: #3665f3;
			}
			.product-info h1 {
				font-size: 24px;
				margin-bottom: 15px;
			}
			.seller-info {
				background-color: #f8f9fa;
				padding: 15px;
				border-radius: 6px;
				margin-bottom: 15px;
			}
			.price {
				font-size: 28px;
				font-weight: bold;
				color: #86b817;
				margin: 20px 0;
			}
			.buttons {
				display: flex;
				flex-direction: column;
				gap: 10px;
			}
			.buttons button {
				padding: 14px;
				border-radius: 6px;
				font-weight: bold;
				cursor: pointer;
				border: none;
				font-size: 16px;
				transition: all 0.3s ease;
			}
			.buy-now-btn {
				background-color: #3665f3;
				color: white;
			}
			.buy-now-btn:hover {
				background-color: #2851d9;
				transform: translateY(-2px);
			}
			.add-cart-btn {
				background-color: white;
				color: #3665f3;
				border: 2px solid #3665f3;
			}
			.add-cart-btn:hover {
				background-color: #eef2ff;
				transform: translateY(-2px);
			}
			.watchlist-btn {
				background-color: white;
				color: #333;
				border: 2px solid #e5e5e5;
			}
			.watchlist-btn:hover {
				border-color: #dcdcdc;
				transform: translateY(-2px);
			}

			/* Similar Items */
			.similar-items {
				margin-top: 30px;
				background-color: white;
				padding: 20px;
				border-radius: 8px;
				box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
				animation: fadeIn 0.8s ease-out;
			}
			.similar-items h2 {
				margin-bottom: 20px;
			}
			.items-grid {
				display: grid;
				grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
				gap: 20px;
			}
			.item-card {
				border: 1px solid #e5e5e5;
				border-radius: 8px;
				padding: 15px;
				text-align: center;
				transition: all 0.3s ease;
			}
			.item-card:hover {
				transform: translateY(-4px);
				box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
			}
			.item-card img {
				width: 100%;
				height: 120px;
				object-fit: contain;
				margin-bottom: 10px;
			}
			.item-card h3 {
				font-size: 16px;
				margin-bottom: 8px;
			}
			.item-price {
				font-size: 18px;
				font-weight: bold;
				color: #86b817;
			}

			/* Footer */
			footer {
				text-align: center;
				padding: 20px;
				margin-top: 30px;
				color: #707070;
			}

			/* Effects */
			.image-zoom-overlay {
				position: fixed;
				top: 0;
				left: 0;
				width: 100%;
				height: 100%;
				background-color: rgba(0, 0, 0, 0.8);
				display: flex;
				align-items: center;
				justify-content: center;
				z-index: 2000;
				cursor: zoom-out;
			}
			.image-zoom-overlay img {
				max-width: 90%;
				max-height: 90%;
			}
			@keyframes fadeIn {
				from {
					opacity: 0;
					transform: translateY(20px);
				}
				to {
					opacity: 1;
					transform: translateY(0);
				}
			}

			/* Mobile Responsive */
			@media (max-width: 768px) {
				.product-section {
					grid-template-columns: 1fr;
				}
				.buttons {
					position: fixed;
					bottom: 0;
					left: 0;
					right: 0;
					background-color: white;
					padding: 15px;
					border-top: 1px solid #e5e5e5;
					box-shadow: 0 -2px 10px rgba(0, 0, 0, 0.1);
					flex-direction: row;
				}
				.container {
					padding-bottom: 100px;
				}
				.items-grid {
					display: flex;
					overflow-x: auto;
					gap: 15px;
					padding-bottom: 10px;
				}
				.item-card {
					min-width: 180px;
					flex-shrink: 0;
				}
				.user-links a:not(:first-child) {
					display: none;
				}
			}
		</style>
	</head>
	<body>
		<header>
			<div class="top-nav">
				<div class="logo"><h2>eBay Clone</h2></div>
				<div class="user-links">
					<a href="#">Hi Friend!</a><a href="#">Daily Deals</a
					><a href="#">Sell</a><a href="#">My eBay</a>
				</div>
			</div>
			<div class="search-area">
				<input type="text" placeholder="Search for anything" /><button>
					Search
				</button>
			</div>
		</header>

		<main class="container">
			<div class="product-section">
				<div class="product-gallery">
					<img
						class="main-image"
						src="https://via.placeholder.com/400x300/4CAF50/white?text=Cool+Toy+Robot"
						alt="Product Image"
					/>
					<div class="thumbnails">
						<img
							class="thumbnail"
							src="https://via.placeholder.com/60x60/4CAF50/white?text=1"
							alt="Thumbnail 1"
						/>
						<img
							class="thumbnail"
							src="https://via.placeholder.com/60x60/2196F3/white?text=2"
							alt="Thumbnail 2"
						/>
						<img
							class="thumbnail"
							src="https://via.placeholder.com/60x60/FF9800/white?text=3"
							alt="Thumbnail 3"
						/>
					</div>
				</div>
				<div class="product-info">
					<h1>Cool Toy Robot</h1>
					<div class="seller-info">
						<p><strong>Seller:</strong> Awesome Toy Store</p>
						<p>99.5% positive feedback</p>
					</div>
					<div class="price">$19.99</div>
					<div class="buttons">
						<button class="buy-now-btn">Buy It Now</button>
						<button class="add-cart-btn">Add to Cart</button>
						<button class="watchlist-btn">Add to Watchlist</button>
					</div>
				</div>
			</div>
			<section class="similar-items">
				<h2>Similar Items</h2>
				<div class="items-grid">
					<div class="item-card">
						<img
							src="https://via.placeholder.com/150x150/9C27B0/white?text=Toy+1"
							alt="Similar Item 1"
						/>
						<h3>Another Cool Toy</h3>
						<p class="item-price">$15.99</p>
					</div>
					<div class="item-card">
						<img
							src="https://via.placeholder.com/150x150/3F51B5/white?text=Game"
							alt="Similar Item 2"
						/>
						<h3>Super Fun Game</h3>
						<p class="item-price">$24.99</p>
					</div>
					<div class="item-card">
						<img
							src="https://via.placeholder.com/150x150/009688/white?text=Puzzle"
							alt="Similar Item 3"
						/>
						<h3>Amazing Puzzle</h3>
						<p class="item-price">$12.99</p>
					</div>
				</div>
			</section>
		</main>

		<footer><p>&copy; 2024 My eBay Clone. Made with ❤️</p></footer>

		<script>
			const thumbnails = document.querySelectorAll(".thumbnail");
			const mainImage = document.querySelector(".main-image");
			const buyNowBtn = document.querySelector(".buy-now-btn");
			const addCartBtn = document.querySelector(".add-cart-btn");
			const watchlistBtn = document.querySelector(".watchlist-btn");
			let isInWatchlist = false;

			thumbnails.forEach(function (thumbnail) {
				thumbnail.addEventListener("click", function () {
					let newImageSrc = thumbnail.src.replace("60x60", "400x300");
					mainImage.src = newImageSrc;
				});
			});

			buyNowBtn.addEventListener("click", function () {
				alert("🎉 Redirecting to checkout! (This is just pretend)");
			});
			addCartBtn.addEventListener("click", function () {
				alert("🛒 Item added to cart! (This is just pretend)");
			});
			watchlistBtn.addEventListener("click", function () {
				if (isInWatchlist) {
					watchlistBtn.textContent = "Add to Watchlist";
					watchlistBtn.style.color = "#333";
					alert("💔 Removed from watchlist");
					isInWatchlist = false;
				} else {
					watchlistBtn.textContent = "In Watchlist ❤️";
					watchlistBtn.style.color = "#e53238";
					alert("❤️ Added to watchlist!");
					isInWatchlist = true;
				}
			});

			mainImage.addEventListener("click", function () {
				const overlay = document.createElement("div");
				overlay.className = "image-zoom-overlay";
				const zoomedImage = document.createElement("img");
				zoomedImage.src = mainImage.src;
				overlay.appendChild(zoomedImage);
				document.body.appendChild(overlay);
				overlay.addEventListener("click", function () {
					document.body.removeChild(overlay);
				});
			});
		</script>
	</body>
</html>
```

## 🚀 What's Next?

Now that you've built this amazing website, here are some fun challenges for you:

1.  **Change the colors and text** to make a page for your favorite toy.
2.  **Add more products** to the "Similar Items" section.
3.  **Find your own pictures** online and use them instead of the placeholders.
4.  **Add a new button** and make it do something new with JavaScript.

## 🏆 You're Now a Web Developer!

You've learned the three main languages of the web:

- **HTML** for the structure (the skeleton)
- **CSS** for styling (the clothes and colors)
- **JavaScript** for interactivity (the actions and magic)

These are the same tools that professional web developers use to build almost every website you visit.

Keep practicing, keep experimenting, and most importantly, keep having fun with code! 🎉
