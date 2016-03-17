## Website Performance Optimization portfolio project

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
- in `style.css`
	- adding `will-change: transform` and `transform: translateZ(0)` to `.mover` so that the moving pizzas in the background are on their own layers 

### No build tools are used in this project.