# Frontend Mentor - Results summary component solution

This my a solution to the [Results summary component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/results-summary-component-CE_K6s0maV). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page

### Screenshot

- Desktop 
![Captura de pantalla 2023-02-22 a las 09 28 35](https://user-images.githubusercontent.com/112894363/220670559-8d428608-3458-41f1-940b-2f2653d62158.png)

- Mobile
![Captura de pantalla 2023-02-22 a las 09 28 49](https://user-images.githubusercontent.com/112894363/220670663-a359073f-5636-44c2-840a-55c79ec52437.png)

### Links

- Solution URL: [https://github.com/bramizdev/fem-results-summary-component](https://github.com/bramizdev/fem-results-summary-component)
- Live Site URL: [https://bramizdev.github.io/fem-results-summary-component/](https://bramizdev.github.io/fem-results-summary-component/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

The challenge for me with this project were the corner borders. I didn't now how to address this problem so I decided to do it with some pseudo elements I added a ```border``` to the parent container, then I created two pseudo elements ```::before``` and ```::after```, for the background I use transparent and I added a ```border: 3px solid white``` and position absolute to cover the parent border.

To see how you can add code snippets, see below:

```html
  <li class="card__summary-category" data-cat="reaction">
    <p>Reaction</p>
    <p class="card__summary-note">
      80 
      <span class="card__summary-max-note">/ 100</span>
    </p>
  </li>
```

```css
.card__summary-category[data-cat='reaction'] {
  color: var(--clr-reaction-500);
  background-color: var(--clr-reaction-500-t);
  border: 1px solid var(--clr-reaction-500-t-br);
  position: relative;
}

.card__summary-category[data-cat='reaction']::before {
  content: '';
  display: block;
  background-color: transparent;
  border-top: 3px solid var(--clr-neutral-100);
  border-bottom: 3px solid var(--clr-neutral-100);
  position: absolute;
  top: var(--corner-br-width);
  bottom: var(--corner-br-width);
  left: var(--corner-br-height);
  right: var(--corner-br-height);
}

.card__summary-category[data-cat='reaction']::after {
  content: '';
  display: block;
  background-color: transparent;
  border-left: 3px solid var(--clr-neutral-100);
  border-right: 3px solid var(--clr-neutral-100);
  position: absolute;
  top: var(--corner-br-height);
  bottom: var(--corner-br-height);
  left: var(--corner-br-width);
  right: var(--corner-br-width);
}

```

### Continued development

I took the idea from this article: [https://codepen.io/ThiemelJiri/post/3-css-border-in-corners-techniques](https://codepen.io/ThiemelJiri/post/3-css-border-in-corners-techniques). I would like to learn more of the other ways to do the corner borders.

### Useful resources

- [https://codepen.io/ThiemelJiri/post/3-css-border-in-corners-techniques](https://codepen.io/ThiemelJiri/post/3-css-border-in-corners-techniques) - This helped me for the corner borders reason. I took the pseudo elements path.

## Author

- Website - [@bramizdev](https://github.com/bramizdev)
- Frontend Mentor - [@bramizdev](https://www.frontendmentor.io/profile/bramizdev)
