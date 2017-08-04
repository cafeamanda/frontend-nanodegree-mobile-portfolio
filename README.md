## Website Performance Optimization portfolio project


### Getting started

1. Clone this repository
2. To inspect the site on your phone, you can run a local server

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```

3. Open a browser and visit localhost:8080
4. Download and install [ngrok](https://ngrok.com/) to the top-level of your project directory to make your local server accessible remotely.

  ``` bash
  $> cd /path/to/your-project-folder
  $> ./ngrok http 8080
  ```

5. Copy the public URL ngrok gives you and try running it through PageSpeed Insights! Optional: [More on integrating ngrok, Grunt and PageSpeed.](http://www.jamescryer.com/2014/06/12/grunt-pagespeed-and-ngrok-locally-testing/)

Profile, optimize, measure... and then lather, rinse, and repeat. Good luck!

#### Part 1: Optimized PageSpeed Insights score for index.html
Scores of 93/100 for mobile and 94/100 for desktop, accomplished by:
* Optimizing large images
* Minifying CSS and JS files
* Loading non-essential scripts asynchronously using tag `async`
* Adding essential CSS directly into the head of index file

#### Part 2: Optimized Frames per Second in pizza.html
* Calling functions `updatePositions()` and `changePizzaSizes()` with `requestAnimationFrame`
* Removing function `determineDx()` entirely and adding switch-case in `changePizzaSizes()` to change sizes accordingly (solution borrowed from Cam's in lesson 8.10)
* Removing all `querySelectorAll` from for loops and pre-calculating all possible layout variables


#### Future optimizations
* Automate minification with grunt/gulp
* Automate image optimization with grunt/gulp
