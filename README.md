To use:

A. Either:
- Clone this repository
- Open the local copy of index.html through a web browser

B. Or:
- Navigate to http://avioane.github.io/views/pizza.html

## Structure
- The original source is in the orig folder
- My changes are in the src folder

####Part 1: Optimized PageSpeed Insights score for index.html

- Minified css and js
- Inlined critical CSS rather than downloading (kept print.min.css separate but added media query)
- Removed comments from JS
- Made the pictures smaller so they can load faster
- Removed linebreaks from the html files

####Part 2: Optimized Frames per Second in pizza.html

- Changed consecutive variable declarations to use the same "var" keyword instead of their own "var" keyword
- resizePizzas function: instead of querySelector, I am using getElementById because querySelector is less efficient;
- changePizzaSizes function: used getElementsByClassName instead of querySelector; instead of grabbing the randomPizzaContainer in the for loop 3 times, moved it outside the for loop
- Moved the declaration of pizzasDiv outside the for loop
- Changed querySelectorAll('.mover'); to getElementsByClassName("mover");
- updatePositions function: Moved document.body.scrollTop / 1250 before the for loop;

### Resources used
https://developer.chrome.com/devtools/docs/tips-and-tricks
https://developers.google.com/web/fundamentals/performance/
Various forum posts from https://discussions.udacity.com/c/nd001-project-4-website-optimization
https://github.com/udacity/fend-office-hours/blob/master/Web%20Optimization/Effective%20Optimizations%20for%2060%20FPS/main.js