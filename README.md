December 2016: Notes

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

9. In function changeSliderLabel, I changed the document.querySelector to document.getElementById on case 1, case 2, and case 3. Reference documentation: https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementById

10. On function determineDx, I changed the var windowWidth from document.querySelector to document.getElementById. I removed the leading (#) when using the JavaScript API call. 

11. With function changePizzaSizes, I declared the variable i before dx. Then I called the [i] variable using the dx variable. In the same function, moved variable declarations for 'dx' and 'newwidth' outside 'for' loop.

12. In function updatePositions, var items, I changed document.querySelectorAll to document.getElementsByClassName removing the (.) inside the previous Javascript API call. 

13. In document.addEventListener ('DOMContentLoaded', function(), the document.getElementById() Web API call is faster. I moved this DOM call outside the for loop statement and saved it into a local variable, which can be used as follows:

/** Outside the loop */
var movingPizzas = document.getElementById('movingPizzas1');

/** Inside the for statement / loop – this line*/
movingPizzas.appendChild(elem);
Reference
https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementById)

14. Declaring the elem variable (var elem;) in the initialisation of the for-loop will prevent it from being created every time the loop is executed.

for (var i = 0, elem; i < 24; i++) {
    elem = document.createElement('img');
    //Other statements
}

15. For function updatePositions(), var scroll, declaring the phase variable (var phase;) in the initialisation of the for loop will prevent it from being created every time the loop is executed.
e.g.

var top = document.body.scrollTop / 1250;

for (var i = 0, len = items.length, phase; i < len; i++) {
    phase = Math.sin(top + i % 5);
    // Other statements
}

16. Decreased size and quality of pizzeria.jpg

17. Finished changes to views/js/main.js file


