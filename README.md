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
- [Acknowledgments](#acknowledgments)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![](./screenshot.png)

### Links

- Solution URL: [Add solution URL here](https://github.com/d4wk0m/Simple-NFT-Show)
- Live Site URL: [Add live site URL here](https://d4wk0m.github.io/Simple-NFT-Show/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties


### What I learned

I've learned how to create modal images using simple JS and CSS. I also learned how to make image ovelays

```html
<div class="overlay">
    <div id="imgo">
        <img src="./images/icon-view.svg"></div>
</div>
```
```css
.overlay {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    height: 100%;
    width: 100%;
    opacity: 0;
    transition: .6s ease;
    background-color: hsla(178, 100%, 50%, 0.692);
    border-radius: 5px;
}

#imgo {
    color: white;
    font-size: 100px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    -ms-transform: translate(-50%, -50%);
    text-align: center;
}

.container:hover .overlay {
    opacity: 1;
}
```
```js
var modal = document.getElementById("myModal");

var img = document.getElementById("imgo");
var img2 = document.getElementById("myImg");
var modalImg = document.getElementById("img01");
var nft = document.getElementById("nft")

img.onclick = function() {
        modal.style.display = "block";
        modalImg.src = img2.src;
        nft.classList.remove("nft2");
    }
var span = document.getElementsByClassName("close")[0];

span.onclick = function() {
    modal.style.display = "none";
    nft.classList.add("nft2");
}
```


### Continued development

I will be focusing on using more flexbox and building more responsive websites

### Useful resources

- [Example resource 1](https://www.example.com) - This helped me for XYZ reason. I really liked this pattern and will use it going forward.
- [Example resource 2](https://www.example.com) - This is an amazing article which helped me finally understand XYZ. I'd recommend it to anyone still learning this concept.

**Note: Delete this note and replace the list above with resources that helped you during the challenge. These could come in handy for anyone viewing your solution or for yourself when you look back on this project in the future.**

## Author

- Website - [Add your name here](https://www.your-site.com)
- Frontend Mentor - [@yourusername](https://www.frontendmentor.io/profile/yourusername)
- Twitter - [@yourusername](https://www.twitter.com/yourusername)

**Note: Delete this note and add/remove/edit lines above based on what links you'd like to share.**

## Acknowledgments

This is where you can give a hat tip to anyone who helped you out on this project. Perhaps you worked in a team or got some inspiration from someone else's solution. This is the perfect place to give them some credit.

**Note: Delete this note and edit this section's content as necessary. If you completed this challenge by yourself, feel free to delete this section entirely.**
