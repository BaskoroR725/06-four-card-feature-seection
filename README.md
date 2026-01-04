# Frontend Mentor - Four card feature section solution

This is a solution to the [Four card feature section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/four-card-feature-section-weK1eFYK).

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size.
- Experience a professional UI with hover states and smooth transitions.

### Screenshot

![](./screenshot.jpg)

*(Note: Don't forget to take a screenshot of your final result and name it screenshot.jpg in your root folder!)*

### Links

- Solution URL: [https://github.com/yourusername/fm-four-card-feature](https://github.com/yourusername/fm-four-card-feature)
- Live Site URL: [https://yourusername.github.io/fm-four-card-feature](https://yourusername.github.io/fm-four-card-feature)

## My process

### Built with

- **Semantic HTML5** - Using landmarks like `<main>`, `<header>`, and `<article>` for better accessibility.
- **Sass (SCSS)** - Organized with a modular architecture (Variables, Reset, Layout, Components).
- **CSS Grid** - Utilized for the complex 3-column "cross" layout on desktop.
- **Flexbox** - Used within components for internal alignment and icon positioning.
- **BEM Methodology** - For clean, maintainable, and scalable class naming.
- **Mobile-first workflow** - Ensuring a solid experience on small screens before scaling up.
- **Modern CSS Features** - Logical properties (`margin-block`), CSS Variables (`:root`), and `clamp()` for responsive typography.

### What I learned

This project was a great refresher on professional CSS architecture. I focused on building a maintainable codebase rather than just "making it look right."

**1. Complex Grid Spanning**
I learned how to use grid lines to create the unique "cross" layout where the side cards span multiple rows while the middle cards are stacked.

```css
.card--cyan {
  grid-column: 1;
  grid-row: 1 / 3;
}
.card--blue {
  grid-column: 3;
  grid-row: 1 / 3;
}

```

**2. Pseudo-elements for UI Detail**
Using ::before to add the colored top border without adding unnecessary div tags in the HTML.

```css
.card {
  position: relative;
  &::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 4px;
  }
}
```

**3. Accessibility (a11y)**
I implemented the prefers-reduced-motion media query to respect users who prefer minimal animations.

```css
@media (prefers-reduced-motion: reduce) {
  .card {
    transition: none;
    transform: none;
  }
}


```

## Author

Baskoro Ramadhan.
