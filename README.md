# Frontend Mentor - Stats preview card component solution

This is a solution to the [Stats preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
- [Author](#author)


## Overview
This mini-project involves the creation of a responsive stats preview card component using plain HTML and CSS.

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size

### Screenshot
![Desktop Interface](./screenshots/desktop-interface.png)
![Mobile Interface](./screenshots/mobile-interface.png)


### Links

- Solution URL: [GitHub Repository](https://github.com/JCBolito/FM-Stats_Preview_Card_Component_Main)
- Live Site URL: [GitHub Pages](https://jcbolito.github.io/FM-Stats_Preview_Card_Component_Main/)

## My process
Breaking down the project into smaller chunks, the following processes were taken to guarantee the project's completion:
1. Structure the HTML.
1. Create the necessary Custom CSS Properties to make the project clean and maintainable.
1. Using a mobile-first approach, tailor the main CSS according to the viewport of a mobile device. 
1. Using media queries, modify the CSS according to the size of a desktop viewport.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow


### What I learned

Upon completing this project, I was again immersed with the Mobile-first approach workflow. Normally, I would do Desktop-first approach, but as a challenge for myself, I went out of my comfort zone and did the project using a Mobile-first approach. To my surprise, I discovered that a Mobile-first approach somehow yields less lines of code compared to a Desktop-first approach.

I was also immersed with the use of the Grid system, as normally, I would use Flexbox system for everything. The Grid system truly is a breath of fresh air, making sure that you place contents exactly where you want them to be.

To make the project maintainable and clean, I utilized Custom CSS Properties which made the code more organized.
```css
:root {
	/* IMAGE FILTER */
	--fltr-img: brightness(50%) sepia(70%) hue-rotate(-130deg) saturate(500%) contrast(.7);
	/* BACKGROUND COLORS */
	--bg-main: hsl(233, 47%, 7%);
	--bg-card: hsl(244, 38%, 16%);

	/* FONT COLORS */
	--fclr-accent: hsl(277, 64%, 61%);
	--fclr-heading: hsl(0, 0%, 100%);
	--fclr-main-paragraph: hsla(0, 0%, 100%, 0.75);
	--fclr-stat-headings: hsla(0, 0%, 100%, 0.6);

	/* FONTS */
	--font-inter: 'Inter', Arial, Helvetica, sans-serif;
	--font-lexend: 'Lexend Deca', Arial, Helvetica, sans-serif;
	font-size: 15px;

	/* SIZES */
	--sz-mobile-card-and-img-width: min(85vw + 1rem, 22rem);
	--sz-section-content-padding: 2rem 2rem 1rem;
	--sz-h1-margin: 1rem 0;
	--sz-h2-margin: 0.25rem 0;
}
```
```css
@media (min-width: 1440px) {
	:root {
		--sz-mobile-card-and-img-width: 90vw;
		--sz-section-content-padding: 5rem;
		--sz-article-content-padding: 0 5rem 5rem;
	}
```
In doing so, I made the project easier to modify and more maintainable compared to my previous ones in which I did not utilize Custom CSS Properties.

I also came across some issues while making the project responsive. A problem I only encountered when using Grid instead of Flexbox.
```css
body {
	height: 100vh;
}
```
Somehow, when I set the height of the body to 100vh, the footer overlaps with the main content at the end of the viewport. Thankfully, I resolved the problem a couple of hours later.
```css
body {
	min-height: 100vh;
}
```
After a couple of hours of trial and error, I discoved that by using min-height instead of height, resolves the said issue.


### Continued development
This is the first project where I utilized Custom CSS Properties and I will probably use it constantly from here on forward. It saved me a lot of time by making my project more maintainable and clean.

I would also keep the issues I encountered here and the solutions that resolved it in mind for future projects if ever I encounter a similar issue.


## Author

- Website - [Joshua Caleb Bolito | JCBolito](https://github.com/JCBolito)
- Frontend Mentor - [@JCBolito](https://www.frontendmentor.io/profile/JCBolito)
- LinkedIn - [Joshua Caleb Bolito](https://www.linkedin.com/in/joshua-caleb-bolito-7a7401214/)