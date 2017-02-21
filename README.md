## Website Performance Optimization portfolio project

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

Project hosted on GitHub: https://pluk74.github.io/frontend-nanodegree-mobile-portfolio/
For PageSpeed Insights score: https://developers.google.com/speed/pagespeed/insights/

####Part 1: Optimize PageSpeed Insights score for index.html

Starting PageSpeed Insights scores:

| Mobile        | Desktop     | 
| ------------- |-------------| 
| 27      | 29 | 

Results:

| Modification | New mobile score | Mobile score change | New desktop score | Desktop score change|
| ------ | ------ | ------ | ------ | ------ |
| Optimize images and resize pizzeria.jpg for index.html | 73 | +46 | 88 | +59 |
| Switch to Webfont loader (asynchronous) | 77 | +4 | 90| +2 |
| Add async to google-analytics js | 77 | 0 | 90| 0 |
| Switch to inline CSS for index.html | 88 | +11 | 94 | +4 |
| Media query for print.css | 95 | +7 | 94 | 0 |

####Part 2: Optimize Frames per Second in pizza.html

1. main.js, line 455: Move query selector and calculations outside of "for" loop.
2. pizza.html, line 4: Switch to inline and minified style.css.
3. Reduced number of moving pizzas from 200 to 24.  The extra pizzas created seemed to be off the viewable area.
4. Scrolled through all Javascript in main.js to look for "for" loops and removed any unnecessary calculations and/or query selectors: lines 476, 510.
5. Switch from querySelector to getElementById: Lines 423, 426, 429, 559.
6. Changed from querySelectorAll to getElementsByClassName: Lines 470, 526.
7. In "for" loops, moved declaration of variables from in the loop to the initialization of the "for" loop.


### Optimization Tips and Tricks
* [Optimizing Performance](https://developers.google.com/web/fundamentals/performance/ "web performance")
* [Analyzing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/analyzing-crp.html "analyzing crp")
* [Optimizing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/optimizing-critical-rendering-path.html "optimize the crp!")
* [Avoiding Rendering Blocking CSS](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css.html "render blocking css")
* [Optimizing JavaScript](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/adding-interactivity-with-javascript.html "javascript")
* [Measuring with Navigation Timing](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/measure-crp.html "nav timing api"). We didn't cover the Navigation Timing API in the first two lessons but it's an incredibly useful tool for automated page profiling. I highly recommend reading.
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/eliminate-downloads.html">The fewer the downloads, the better</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer.html">Reduce the size of text</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization.html">Optimize images</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching.html">HTTP caching</a>

### Customization with Bootstrap
The portfolio was built on Twitter's <a href="http://getbootstrap.com/">Bootstrap</a> framework. All custom styles are in `dist/css/portfolio.css` in the portfolio repo.

* <a href="http://getbootstrap.com/css/">Bootstrap's CSS Classes</a>
* <a href="http://getbootstrap.com/components/">Bootstrap's Components</a>
