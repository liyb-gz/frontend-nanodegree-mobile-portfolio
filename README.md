# Website Performance Optimization portfolio project

## Getting Started
1. Download the ZIP file from github (come on, you can find the "Download ZIP" button!)
2. Unzip the compress file
3. Open the unzipped folder
4. Double click on the `index.html` file
5. Enjoy staring at our dear Mr. Cameron Pittman!
6. Click on the link `Cam's Pizzeria`
7. Enjoy staring at the pizzas! They are everywhere!!!

## Optimizations Summary

### Part 1: Optimize PageSpeed Insights score for index.html

The below optiomizations have been done to the index.html:

- Resizing images
- Adding `async` propety to analytic scripts
- Adding `media="print"` to print stylesheet
- Inlining important stylesheets into `index.html`
- Minifing `.css` and `.js` files
- Minifing the `index.html` file

**Note**: As this project only asks for optimizing index.html, I compressed all the files mentioned by PageSpeed and simply ignored the effects to other pages (otherwise there are no ways to achieve the 90+ speed score). 

### Part 2: Optimize Frames per Second in pizza.html

The below optiomizations have been done to the pizza.html:

- in `main.js`
	- caching `document.body.scrollTop` so that it is requested only once
	- refactoring the way the new width of the pizzas is calculated.
	- refactoring the function for updating random pizzas so the widths are now in percentage.
	- refactoring the generation of moving pizzas on page load, so only visible pizzas are created.
	- refactoring the update function for moving pizzas' positions, so it won't query the DOM in the `for` loops
	- replacing `document.querySelector` with the more efficient `document.getElementbyID`
	- replacing `document.querySelectorAll` with the mroe efficient `document.getElementsbyClassName`
- in `style.css`
	- adding `will-change: transform` and `transform: translateZ(0)` to `.mover` so that the moving pizzas in the background are on their own layers 

### No build tools are used in this project.