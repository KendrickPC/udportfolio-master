December 2016: Notes

<!-- Non-optimized code inside for-loops has its mistakes multiplied by the factor "i"! — therefore optimizng the loop code is one of the most important things you can do for performance optimization! -->
https://discussions.udacity.com/t/project-4-how-do-i-optimize-the-background-pizzas-for-loop/36302

<!-- It has been observed that functions like querySelector and querySelectorAll are not as efficient as their fellow Vanilla JS DOM-querying functions getElementById, getElementsByClassName, and getElementsByTagName. -->
https://jsperf.com/getelementsbyclassname-or-queryselectorall

----------------------------------------------------------------------------------

## Website Performance Optimization portfolio project

### Getting started

1. Check out the project Git repository
2. Run a local server
  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```
3. Open a browser and visit localhost:8080
4. Download and install [ngrok](https://ngrok.com/) to make your local server accessible remotely.
  ``` bash
  $> cd /path/to/your-project-folder
  $> ./ngrok 8080
  ```
5. Copy the public URL ngrok gives you and try running it through PageSpeed Insights! [More on integrating ngrok, Grunt and PageSpeed.](http://www.jamescryer.com/2014/06/12/grunt-pagespeed-and-ngrok-locally-testing/)
6. Run developer tools in your browser. Check the console for Time to Generate Pizzas On Load and Average Scripting Time for Last 10 Frames.
7. Place "use strict"; as the first line on the main.js file. 
8. Moved variables i, dx, and newwidth outside the 'for' loop in the changePizzaSizes(size) function. Make sure to remeasure the scripting time to compare the time saved. 
9. 



Profile, optimize, measure... and then lather, rinse, and repeat. Good luck!

### Optimization Tips and Tricks


