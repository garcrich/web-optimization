# Website Performance Optimization Portfolio Project

The objective of this project was to test the student’s ability to improve an extremely inefficient website. Supporting courses included Website Performance Optimization and Browser Rendering Optimization. 

#Requirements

Achieving a Google PageSpeed of 90 or above and a FPS of 60 for pizza-min.html

#Access Website

To access the website, copy and paste the following url into your browsers address bar:

http://garcrich.github.io/web-optimization/

#How optimizations were made

##Index.html Page Display

* CSS was inlined to remove render blocking.
* All css was minifyied to reduce bytes for faster parsing.
* JS files for index.html were given the async attribute to remove render blocking.
* images were reduced to thumbmail size and compressed to reduce file size.
* Google fonts was removed to remove render blocking and downloading. Affect on text was marginal
* CSS element tags were replaced with faster element or class tags. 
* css/style-print.css was given the media tag `print` to remove render blocking.
* Comments removed.

##pizza.html Page Display (browser runs pizza-min.html)

* Reduced and compressed images.
* Provided more specific tags for faster rendering.
* Inlined CSS to remove render blocking.
* Minified bootstrap-grid.css to bootstrap-grid-min.css.
* added `will-change: transform` and `translateZ(0);` to force seperate layers for classes mover and randomPizzaContainer.
* Replaced for while loop for for makeRandomPizza with while (var --) for faster rendering.
* Replaced all `document.querySelector` methods with more specific methods such as `document.getElementsByClassName`.
* Simplified `changePizzaSizes(size)` function.
* Reduced Forced Synchronous Layout be declaring variables outside of for loops. See example here [https://www.udacity.com/course/viewer#!/c-ud860-nd/l-4147498575/e-4154208580/m-4240308553]
* Reduced number of randomly generated pizzas that appeared on screen as well as pizzas in the background.

#How to Test Requirements


##PageSpeed Insights

Visit:

https://developers.google.com/speed/pagespeed/insights/

copy and paste

http://garcrich.github.io/web-optimization

Into analyze field.

##FPS for pizza-min.html

1. From the homepage select Cam's Pizzeria within the Chrome web browser. 
2. Open Google developer tools.
3. Under enable Rendering tab (press Esc if not shown) check the option "Show FPS meter"
4. In the top right corner FPS stats will be shown. 
5. Scroll on the page to see if FPS 60 can be obtained.
