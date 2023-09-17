# These code can save your time

## Adds the "active" class to the navbar when the user scrolls down the page.

```js
// js/navbar.js

// Get the navigation bar element from the DOM
const nav = document.querySelector("#nav");

// Create a scroll event listener
const onScroll = (event) => {
  // Get the current scroll position
  const scrollPosition = event.target.scrollingElement.scrollTop;

  // If the scroll position is greater than 10px
  if (scrollPosition > 10) {
    // If the navigation bar does not have the "scrolled-down" class
    if (!nav.classList.contains("scrolled-down")) {
      // Add the "scrolled-down" class to the navigation bar
      nav.classList.add("scrolled-down");
    }
  } else {
    // If the navigation bar has the "scrolled-down" class
    if (nav.classList.contains("scrolled-down")) {
      // Remove the "scrolled-down" class from the navigation bar
      nav.classList.remove("scrolled-down");
    }
  }
};

// Add the scroll event listener to the document
document.addEventListener("scroll", onScroll);
```
