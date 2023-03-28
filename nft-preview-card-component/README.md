# Frontend Mentor - NFT preview card component solution

This is a solution to the [NFT preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/nft-preview-card-component-SbdUL_w0U). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

This is my 4th component project completed from Frontend Mentor.

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![Screenshot](./images/screenshot.png)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

- Reviewed the style-guide and mockup images
- Created html and css files, then added root section with style guide elements to CSS file
- Formatted HTML using Flexbox
- Filled in default and standardized CSS attributes to img, h2, and p elements
- Worked on image overlay for interactive image
- Launched page and begin adjusting margin, padding and border until I was happy with the look for the desktop view
- Repeated last step for mobile view and wrapped up with tweaks to the scale of the container on widths between media screens

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox

### What I learned

Learning how to set up a hover overlay on the image was new to me this project. I learned how to do so using opacity and a pseudo class (hover).

```html
<div class="imageContainer">
  <img src="./images/image-equilibrium.jpg" alt="equilibrium" class="image">
  <div class="overlay overlayFade"></div>
  <div class="view viewHover"></div>
</div>
```
```css
.overlay {
  position: absolute;
  transition: all 0.3s ease;
  opacity: 0;
  background-color: var(--cyan);
  border-radius: 10px;
}

.view {
  position: absolute;
  transition: all 0.3s ease;
  opacity: 0;
  background-image: url(./images/icon-view.svg);
  background-size: cover;
}

.imageContainer:hover .overlay {
  opacity: 0.5;
}

.imageContainer:hover .view {
  opacity: 1;
}

.overlayFade {
  height: 310px;
  width: 310px;
  top: 0;
  left: 0;
  background-color: var(--cyan);
}

.viewHover {
  width: 50px;
  height: 50px;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```
### Continued development

I want to mess around with different overlay behaviors for a flashier look on hover like sliding the overlay in directionally or radially.

### Useful resources

- [Geeks for Geeks](https://www.geeksforgeeks.org/how-to-create-image-overlay-hover-using-html-css/) - This helped me learn how to add the overlay effect on image hover. I will continue to use this technique for vanilla CSS overlays.


## Author

- Frontend Mentor - [@mylesh-portfolio](https://www.frontendmentor.io/profile/myles-portfolio)
- Medium - [@mylesh_](https://medium.com/@mylesh_)
