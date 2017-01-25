December 2016: Notes

----------------------------------------------------------------------------------

## Website Performance Optimization portfolio project

### Getting started

<<<<<<< HEAD
1. Check out the project Git repository
||||||| merged common ancestors
Some useful tips to help you get started:

1. Check out the repository
1. To inspect the site on your phone, you can run a local server
=======
Some useful tips to help you get started:

1. Check out the repository
2. To inspect the site on your phone, you can run a local server
>>>>>>> 2d64a779e4792be57dd51c4a24df5923605d3a0e

2. Run a local server
  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8000
  ```
3. Open a browser and visit localhost:8080

<<<<<<< HEAD
4. Download and install [ngrok](https://ngrok.com/) to make your local server accessible remotely.
||||||| merged common ancestors
1. Open a browser and visit localhost:8080
1. Download and install [ngrok](https://ngrok.com/) to make your local server accessible remotely.

=======
3. Open a browser and visit localhost:8000
4. Download and install [ngrok](https://ngrok.com/) to make your local server accessible remotely.

>>>>>>> 2d64a779e4792be57dd51c4a24df5923605d3a0e
  ``` bash
  $> cd /path/to/your-project-folder
<<<<<<< HEAD
  $> ./ngrok 8080
||||||| merged common ancestors
  $> ngrok 8080
=======
  $> ./ngrok 8000
>>>>>>> 2d64a779e4792be57dd51c4a24df5923605d3a0e
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

<<<<<<< HEAD
for (var i = 0, len = items.length, phase; i < len; i++) {
    phase = Math.sin(top + i % 5);
    // Other statements
}
||||||| merged common ancestors
1. Copy the public URL ngrok gives you and try running it through PageSpeed Insights! [More on integrating ngrok, Grunt and PageSpeed.](http://www.jamescryer.com/2014/06/12/grunt-pagespeed-and-ngrok-locally-testing/)
=======
5. Added "use strict"; to the top of JS File
Reference: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode
6. changeSliderLabel(size) function --> Changed document.querySelector to getElementById on case 1,2, and 3. This reduces time to generate pizzas on load by for the first 10 frames. 
Reference: https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementById
7. In function determineDx, the variable windowWidth webAPI call to querySelector was changed to getElementById. 
8. Placed variable i above variable dx in function changePizzaSizes so that i can be declared before running dx
9. Changed updatePositions function variable items from querySelector to getElementById JS API call. Removed the period in front of 'mover'.
10. 



-----------------------------------------------------------------------

1. Copy the public URL ngrok gives you and try running it through PageSpeed Insights! [More on integrating ngrok, Grunt and PageSpeed.](http://www.jamescryer.com/2014/06/12/grunt-pagespeed-and-ngrok-locally-testing/)
>>>>>>> 2d64a779e4792be57dd51c4a24df5923605d3a0e

16. Decreased size and quality of pizzeria.jpg

### Optimization Tips and Tricks


