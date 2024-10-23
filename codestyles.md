# Front-End Development Code Standards

## Table of Contents
1. **General Principles**
2. **HTML Coding Standards**
3. **CSS Coding Standards**
4. **JavaScript Coding Standards**
5. **Performance Optimization**
6. **Accessibility**
7. **Responsive Design**
8. **Commenting and Documentation**

---

### 1. General Principles

**a. Consistency**: Maintain a consistent coding style throughout your project.

**b. Readability**: Write clean, well-organized code that is easy to understand and maintain.

**c. Separation of Concerns**: Keep HTML, CSS, and JavaScript separate as much as possible. Use external stylesheets and scripts.

### 2. HTML Coding Standards

**a. Doctype Declaration**: Always include the HTML5 doctype at the top of your documents.
```html
<!DOCTYPE html>
```

**b. Language Attribute**: Specify the language of the document.
```html
<html lang="en">
```

**c. Semantic Markup**: Use semantic HTML5 elements to enhance readability and accessibility.
```html
<header>, <main>, <footer>, <article>, <section>
```

**d. Attribute Usage**: Use double quotes for attribute values and maintain a consistent attribute order.
```html
<input type="text" placeholder="Enter your name">
```

**e. Indentation and Formatting**: Use 2 spaces for indentation and keep your code formatted for readability.
```html
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
</ul>
```

**f. Naming Conventions**: Use lowercase, hyphen-separated names for IDs and classes.
```html
<div id="main-content" class="container-fluid">
```

**g. Forms**: Use `<form>` elements with appropriate `action` and `method` attributes. Wrap labels and inputs in `<div class="form-group">` for better styling.
```html
<form action="/submit" method="post">
  <div class="form-group">
    <label for="username">Username</label>
    <input type="text" id="username" name="username" class="form-control">
  </div>
  <!-- Add more form fields as needed -->
</form>
```

### 3. CSS Coding Standards

**a. External Stylesheets**: Use external CSS files to keep styles separate from HTML.
```html
<link rel="stylesheet" href="styles.css">
```

**b. Naming Conventions**: Use camelCase for class names and IDs. Avoid using overly specific selectors.
```css
.main-content {
  /* Styles here */
}
```

**c. Specificity**: Keep CSS specificity low to ensure maintainability.
```css
/* Good */
.button {
  background-color: blue;
}

/* Bad */
div.button.submit-button {
  background-color: blue;
}
```

**d. Responsive Design**: Use media queries to create responsive layouts.
```css
@media (max-width: 768px) {
  .container {
    flex-direction: column;
  }
}
```

### 4. JavaScript Coding Standards

**a. External Scripts**: Use external JavaScript files to keep scripts separate from HTML.
```html
<script src="scripts.js"></script>
```

**b. Variable Naming**: Use camelCase for variable and function names.
```javascript
let myVariable = 10;
function myFunction() {
  // Code here
}
```

**c. Avoid Inline Scripts**: Avoid using inline JavaScript within HTML tags.
```html
<!-- Bad -->
<button onclick="alert('Hello!')">Click me</button>

<!-- Good -->
<button id="myButton">Click me</button>
<script>
  document.getElementById('myButton').addEventListener('click', function() {
    alert('Hello!');
  });
</script>
```

**d. Use Strict Mode**: Use strict mode to catch common coding mistakes.
```javascript
'use strict';
```

### 5. Performance Optimization

**a. Minimize HTTP Requests**: Combine CSS and JavaScript files to reduce the number of HTTP requests.

**b. Minification**: Minify CSS, JavaScript, and HTML to reduce file sizes.

**c. Caching**: Use caching strategies to minimize reload times.

**d. Image Optimization**: Compress images to improve load times.

### 6. Accessibility

**a. ARIA Roles**: Use ARIA roles to enhance accessibility when necessary.
```html
<div role="navigation">
  <!-- Navigation links -->
</div>
```

**b. Alt Attributes**: Always provide `alt` attributes for images.
```html
<img src="image.jpg" alt="Description of image">
```

**c. Keyboard Navigation**: Ensure interactive elements are accessible via keyboard.

### 7. Responsive Design

**a. Meta Viewport**: Use the `viewport` meta tag to ensure your pages are responsive.
```html
<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
```

**b. Flexbox and Grid**: Use Flexbox and CSS Grid for creating flexible and responsive layouts.

### 8. Commenting and Documentation

**a. Explanatory Comments**: Comment your code to explain complex sections, hacks, or workarounds.
```html
<!-- Main navigation starts here -->
<nav>
  <!-- Navigation links -->
</nav>
<!-- Main navigation ends here -->
```

**b. TODO Comments**: Use `TODO` comments for items that need to be addressed later.
```html
<!-- TODO: Add responsive styles for this section -->
```

**c. JavaScript Comments**: Use comments in JavaScript to explain functions, logic, and complex operations.
```javascript
// Function to calculate the sum of two numbers
function calculateSum(a, b) {
  return a + b;
}
```
