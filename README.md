# Mad Libs

## What is Mad Libs

You might have played it before where it is a word game that consists of a player prompting others for a list of words to fill in the blanks of a story before reading it outloud. In this project you will be using functions to create stories and prompting users (yourself or others) to enter input based on the story. These inputs could be adjectives, nouns, verbs, vehicles, food items, etc.


## Part I: HTML
- In `index.html` create a div tag with class container.
- Within that div tag create 3 other div tags with class category. These will represent your 3 different stories.
- Each of those div tags will have a ``<img>``, ``<p>``, and ``<button>`` tags inside of them.

- In one of the div tags:
    - Create a ``<img>`` tag and get `dinner.jpg` from the images folder.
    - (Optional) Set the alt to dinner.
    - Create a ``<p>`` tag and paste in the following:
    ```plaintext
    You have been invited to the most bizarre dinner party in town filled with unexpected twists, peculiar foods, and outrageous events.
    ```
    - Create a ``<button>`` tag and inside the tag paste in the following:
    ```plaintext
    Generate Dinner Story!
    ```
    - We want the button to do something when someone clicks on it so within the button tag, create an onclick event in which when the user clicks the button, it will run a function which will be implemented later, for now leave the onclick event blank. This is what it will look like:

    ```html
    <button onclick="">Generate Dinner Story</button>
    ```

- In another div tag:
    - Create an ``<img>`` tag and get the `mystery.jpg` from the images folder.
    - (Optional) Set the alt to mystery.
    - Create a ``<p>`` tag then copy and paste the following:
    ```plaintext
    Enter the world of cobblestone streets, candlelit mansions, and peculiar characters, where a shocking crime shakes Victorian high society. A dashing yet delightfully unconventional detective must piece together the puzzle, navigating a cast of absurd suspects and hilariously bizarre clues.
    ```
    - Create a ``<button>`` tag with an onclick event then copy and paste the following in the button tag:
    ```plaintext
    Generate Mystery Story!
    ```
- In the last div tag:
    - Do the same thing and get the `time_travel.jpg` from the images folder.
    - (Optional) Set the alt to travel.
    - Copy and paste the following:
    ```plaintext
    Your malfunctioning time machine has created total chaos in the space-time continuum! Someone has used it to steal your homework before it was even due. It is up to you to travel through time and get it back before the bell rings for class.
    ```
    - Create a ``<button>`` tag with onclick then copy and paste the following:
    ```plaintext
    Generate Time Travel Story!
    ```
- Outside the div tag with the class container create a ``<h3>`` tag and paste in the following:
```plaintext
Your Generated Story
```
- Lastly, outside of the div tag with class container, create a div tag with an id of output. You can leave it blank.


## Part II: CSS
- For now your website will look kind of funky with big images and text not aligning properly.
- In `style.css` we want the header's (the ``<h1>`` and ``<h2>`` tags) to be in the center of our website (Hint: Use Flexbox!).
- First off the images are way to big, we need to resize it.
- Style all images to have the following:
    - `width` of 100%
    - `height` set to auto. You can just type `auto`.
    - `border-radius` to about 25 pixels.
        - This will round the corners for images.
    - `margin-bottom` to about 10 pixels. 
        - This will help space between the images and text.

- Style all paragraphs ``<p>`` to have the following:
    - `font-size` of 16 pixels.
    - `line-height` of 1.5.

- Style all buttons ``<button>`` to have the following:
    - `padding` of 10 pixels.

### ---- Feel free to change any of the values or add additional styling elements! ----

After all that, your website should look similar to this:

![demo](demo.jpg)

## Part III: JavaScript
- In the `script.js` you will implement 3 functions that will be added to the onclick event in the `index.html` file.
- Create a function named `dinner` with no parameters.
- Inside the dinner function you will create variables that takes in user input by using the `prompt` method which looks something like this:
```js
const varName = prompt("Question goes here...");
```
- Create 8 variables that prompts the users to enter the following (in parentheses) from this story:
```plaintext
The dinner party started with a dish of (FOOD) that smelled like (SOMETHING STRANGE). 
Suddenly, a (ADJECTIVE) (ANIMAL) appeared and started (VERB) on the table! 
The host grabbed a (OBJECT) and yelled "(FUNNY QUOTE)!" 
We all laughed and said "(ANOTHER FUNNY QUOTE)." It was unforgettable!
```
- Here is an example of what your variables should look like:
```js
const food = prompt("Name a food item");
```
- Next we need to ensure that the user has inputted something in all of the 8 variables. We will use `if` and `else` statements.
- Here is the format of `if` and `else` statements in JavaScript:
```js
if (condition)
{
    // Run this part of code
}
else
{
    // Run this part instead
}
```
- Create a condition to check if the user inputted something for all 8 of the variables. You can do this by using the AND operator `&&`:
```js
if (condition1 && condition2 && ...) //<-- if condition 1 and condition 2 are true then run the code below otherwise run the code in the else statement.
{
    // Run this part of code
}
else
{
    // Run this part instead
}
```
- If your stuck on this here is a hint:
    - Go to this website --> https://www.geeksforgeeks.org/explain-the-concept-of-truthy-falsy-values-in-javascript/
    - Scroll down all the way to the header that says "What are Falsy Values".
    - In summary if the user clicks cancel on the prompt it will generate a `null` value indicating that the variable has not been assigned a value. This would cause a false statement in the if statement.
    - If the user clicks okay but never inputted anything, it will generate a `""` or an empty string which would also cause a false statement in the if statement.
    - If this is still too confusing please ask a question :)

- In the if statement copy and paste the following:
- ```js
  document.getElementById("output").innerHTML = `
  <p>The dinner party started with a dish of (FOOD) that smelled like (SOMETHING STRANGE). 
  Suddenly, a (ADJECTIVE) (ANIMAL) appeared and started (VERB) on the table! 
  The host grabbed a (OBJECT) and yelled "(FUNNY QUOTE)!" 
  We all laughed and said "(ANOTHER FUNNY QUOTE)." It was unforgettable!</p>
  `;
  ```
- You don't need to know what everything does but basically it finds the HTML element with an id of output, then the `.innerHTML` replaces the contents inside the element with a new string of HTML.

    - So if my JavaScript was:
    - ```js
      document.getElementById("output").innerHTML = `<p> Hello World </p>`;
      ```

    - The HTML will go from this:
    - ```html
      <div id="output"></div>
      ```
    - To this:
    - ```html
      <div id="output">
        <p> Hello World </p>
      </div>
      ```
- Remove the parentheses including everything inside the parentheses and replace it with `${yourVariableName}`
- This will replace the parentheses with the given user input.
- Do this for all 8 of the other placeholders.
- In the else statement paste in the following:
- ```js
  alert("Oops! You missed one or more inputs. Please try again!");
  ```
- This will alert the user if they did not fill out all 8 of the variables.

### Once you got this down, doing the next 2 functions will be fairly easy.

- Create a function named `mystery` with no parameters.
- Create 11 variables that prompts the users to enter the following (in parentheses) from this story:
```plaintext
On a(n) (ADJECTIVE) night in the grand (PLACE), a loud (SOUND) revealed Lord (SILLY NAME 1) lying beside a (OBJECT), muttering, "It was the (NOUN)!"
Detective (NAME), questioned the (JOB TITLE), who was caught (VERB) near the scene. But the truth was stranger than fiction.
It turns out Lord (SILLY NAME 1) had slipped on (SUBSTANCE) while trying to steal a plate of (FOOD).
Everyone laughed, and the detective vowed to investigate only serious cases from now on.
```
- Next ensure that the user has inputted something in all of the 11 variables using `if` and `else` statements.
- In the `if` statement paste in the following and replace the placeholders with your variable names using `${yourVariableName}`.
- ```js
   document.getElementById("output").innerHTML = `
   <p>On a(n) (ADJECTIVE) night in the grand (PLACE), a loud (SOUND) revealed Lord (SILLY NAME 1) lying beside a (OBJECT), muttering, "It was the (NOUN)!"
   Detective (NAME), questioned the (JOB TITLE), who was caught (VERB) near the scene. But the truth was stranger than fiction. 
   It turns out Lord (SILLY NAME 1) had slipped on (SUBSTANCE) while trying to steal a plate of (FOOD).
   Everyone laughed, and the detective vowed to investigate only serious cases from now on.</p>
   `;
   ```
- In the else statement paste in the following:
- ```js
  alert("Oops! You missed one or more inputs. Please try again!");
  ```

## 

- Lastly create a function named `travel` with no parameters.
- Create 9 variables that prompts the users to enter the following (in parentheses) from this story:
```plaintext
Your time machine malfunctions, and a (HISTORICAL FIGURE) steals your homework escaping to (PLACE)!
Armed with a (OBJECT), you chase them through time, dodging (PLURAL NOUN) and a (ADJECTIVE 1) dinosaur trying to (VERB) you.
You finally catch the thief at (EVENT IN TIME) and grab your homework just time.
Back in class, your teacher, (SILLY NAME), says, "That's the most $(ADJECTIVE 2) excuse ever!" But hey, you got an A!
```
- Next ensure that the user has inputted something in all of the 9 variables using `if` and `else` statements.
- In the `if` statement paste in the following and replace the placeholders with your variable names using `${yourVariableName}`.
- ```js
  document.getElementById("output").innerHTML = `
  <p>Your time machine malfunctions, and a (HISTORICAL FIGURE) steals your homework escaping to (PLACE)!
  Armed with a (OBJECT), you chase them through time, dodging (PLURAL NOUN) and a (ADJECTIVE 1) dinosaur trying to (VERB) you.
  You finally catch the thief at (EVENT IN TIME) and grab your homework just time.
  Back in class, your teacher, (SILLY NAME), says, "That's the most (ADJECTIVE 2) excuse ever!" But hey, you got an A!</p>
  `;
  ```
- In the else statement paste in the following:
- ```js
  alert("Oops! You missed one or more inputs. Please try again!");
  ```

## Part IV: Linking
- Go back to the `index.html` file and call the function `dinner()`, `mystery()`, and `travel()` by putting these functions inside the quotation marks within the `onclick` events.
- Check that everything works by pressing the buttons, entering user input, leaving inputs blank, etc.
- Your outputted story with user input will be displayed below at the bottom of the page.

        