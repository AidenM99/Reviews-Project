## Table of contents

- [Overview](#overview)
  - [The project](#the-project)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)

## Overview

### The challenge

- The aim of this project was to create a dashboard of reviews with the added functionality of allowing the user to scroll forwards and backwards through
the reviews or to be surprised with a random review upon clicking the corresponding button.

### Screenshot

![](./ReviewsProject.png)

### Links

- Live Site URL: 

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- JavaScript

### What I learned

- How to cycle through objects to create a loop

```js
document.querySelector(".next-btn").addEventListener("click", function() {
  currentItem++;
  if (currentItem>reviews.length-1){
    currentItem=0;
  };
  personInfo();
});

document.querySelector(".prev-btn").addEventListener("click", function() {
  currentItem--;
  if (currentItem<0){
    currentItem=3;
  };
  personInfo();
});

document.querySelector(".random-btn").addEventListener("click", function(){
  currentItem = Math.floor(Math.random()*4);
  personInfo();
});
```

- How to create an array of objects

```js
var reviews = [{
    id: 1,
    name: "susan smith",
    job: "web developer",
    img: "https://res.cloudinary.com/diqqf3eq2/image/upload/v1586883334/person-1_rfzshl.jpg",
    text: "I'm baby meggings twee health goth +1. Bicycle rights tumeric chartreuse before they sold out chambray pop-up. Shaman humblebrag pickled coloring book salvia hoodie, cold-pressed four dollar toast everyday carry",
  },
  {
    id: 2,
    name: "anna johnson",
    job: "web designer",
    img: "https://res.cloudinary.com/diqqf3eq2/image/upload/v1586883409/person-2_np9x5l.jpg",
    text: "Helvetica artisan kinfolk thundercats lumbersexual blue bottle. Disrupt glossier gastropub deep v vice franzen hell of brooklyn twee enamel pin fashion axe.photo booth jean shorts artisan narwhal.",
  },
];
```

- How to dynamically display what is shown on-screen by selecting properties in an array instead of hard coding in HTML

```js
var img = document.querySelector("#person-img");
var author = document.querySelector("#author");
var job = document.querySelector("#job");
var text = document.querySelector("#info");

function personInfo(){
var item = reviews[currentItem];
img.src = item.img;
author.textContent = item.name;
job.textContent = item.job;
text.textContent = item.text;
};
```

### Continued development

- I plan to keep honing my JavaScript skills, building projects to do so in order to become more competent at the language as a whole.

