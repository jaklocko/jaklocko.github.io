# Udacity Web Optimization Project

This project is designed to teach web optimization techniques to ensure pages render as quickly and efficiently as possible. Students were tasked with modifying javascript, css, and html files in order to provide a fast, responsive user experience. Some changes made are outlined below:

### index.html
* Added media rules to CSS files to ensure only necessary content is requested at page load
* Created separate script files for various scripts
  * Added async/defer to scripts as needed
* Minified whole file
* Inline-ed CSS as appropriate
* Integrated Web Font Loader to load fonts asynchronously
* Optimized all images using File Optimizer [File Optimizer](http://nikkhokkho.sourceforge.net/static.php?page=FileOptimizer)

### pizza.html
* Minified file
* Added async to main.js script call

### main.js
* Removed determineDX function since it was, as Cam stated, Utterly useless
* Refactored changePizzaSizes function according to previous work in the Styling and Layout course to remove Forced Synchronous Layout code
* Refactored "for-loop actually creates and appends all of the pizzas when the page loads" function by moving variable declaration out of the loop


_Pagespeed insights consistently reports a 95/96 for Mobile/Desktop for my index.html page_
_pizza.html resizes pizzas in under 1 ms, and consistently scrolls at 60 FPS_

_Minifiers/beautifiers used:_
* [Dirty Markup](https://dirtymarkup.com/)
* [JSHint](http://jshint.com/)
* [W3 HTML Validator](https://validator.w3.org)
* [W3 CSS Validator](http://jigsaw.w3.org/css-validator/)
