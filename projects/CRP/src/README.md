# Udacity Web Optimization Project

This project is designed to teach web optimization techniques to ensure pages render as quickly and efficiently as possible. Students were tasked with modifying javascript, css, and html files in order to provide a fast, responsive user experience. Some changes made are outlined below:

### index.html
* Added media rules to CSS files to ensure only necessary content is requested at page load
* Created separate script files for various scripts
  * Added async/defer to scripts as needed
* Minified whole file
* Inline-ed CSS as appropriate
* Integrated Web Font Loader to load fonts asynchronously
* Optimized all images using [File Optimizer](http://nikkhokkho.sourceforge.net/static.php?page=FileOptimizer)

### pizza.html
* Minified file
* Added async to main.js script call

### main.js
* Removed determineDX function since it was, as Cam stated, Utterly useless
* Refactored changePizzaSizes function according to previous work in the Styling and Layout course to remove Forced Synchronous Layout code
* Refactored "for-loop actually creates and appends all of the pizzas when the page loads" function by moving variable declaration out of the loop
* Refactored updatePositions to use document.getElementsByClassName instead of document.querySelectorAll for performance reasons
	* Moved non-changing values into variable declarations outside of loop
* Moved code to generate the background pizzas outside of anonymous function, thus allowing the function to be called when the window is resized.
	* Refactored code to move container selection outside of loop, determine the viewport height, number of necessary rows of pizzas, then total number of necessary pizzas to fill the background


## Pagespeed insights consistently reports a 95/96 for Mobile/Desktop for my index.html page
## pizza.html resizes pizzas in under 1 ms, and consistently scrolls at 60 FPS
