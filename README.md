# Mad Libs

## What is Mad Libs

You might have played it before where it is a word game that consists of a player prompting others for a list of words to fill in the blanks of a story before reading it outloud. In this project you will be using functions to create stories and prompting users (yourself or others) to enter input based on the story. These inputs could be adjectives, nouns, verbs, vehicles, food items, etc.


## Part I: HTML

### Step 1
In `index.html` create a div tag with a class and name it `container`. Here is a reminder of what a div tag with a class looks like:
```html
<div class="classNameGoesHere">
    <!-- Some Code -->
</div>
```
Inside that div tag create 3 other div tags with class category. These will represent your 3 different stories.

> [!NOTE]
> If you want to know if you're on the right track, below is the solution to step 1. These solutions will be at the end of every step to ensure you understand it and your website functions as expected.

<details>
<summary>Step 1 Solution</summary>

```html
<!-- Start writing code below -->
<div class="container">
    <div class="category">
        <!-- Implement in Step 2 -->  
    </div>

    <div class="category">
        <!-- Implement in Step 3 -->  
    </div>
  
    <div class="category">
        <!-- Implement in Step 4 -->  
    </div>
</div>
```
</details>

### Step 2
Each of those div tags will have a ``<img>``, ``<p>``, and ``<button>`` tags inside of them. Here is a reminder of what these tags look like:

```html  
<!-- image tag -->
<img src="sourcePath" alt="">

  <!--
    - src: the path to the image
    - alt: alternate text to image (will show text if image cannot be displayed) 
  -->

<!-- paragraph tag -->
<p>Text goes here</p>

<!-- button tag -->
<button onclick="function()">Text goes here</button>

  <!--
    - onclick: when the user clicks on the button do something
  -->
```                                  

In one of the div tags:
- Create a ``<img>`` tag and get `dinner.jpg` from the images folder.
> [!NOTE] 
> Remember from week 2 that talks about file paths? Find a file path to go from the images folder then to the `dinner.jpg` image. Once you found the path, put it in `src` of the image tag.

> [!TIP]
> You know that you got the correct path when the image is shown on your website.
- Set the alt to dinner.
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
<button onclick="">Generate Dinner Story!</button>
```

<details>
<summary>Step 2 Solution</summary>

```html
<div class="category">
    <img src="images/dinner.jpg" alt="dinner">
    <p>You have been invited to the most bizarre dinner party in town filled with unexpected twists, peculiar foods, and outrageous events.</p>
    <button onclick="">Generate Dinner Story!</button>
</div>
``` 
</details> 

> [!IMPORTANT]
> If you can understand step 2 then step 3 and 4 will be easy since it is the basically the same.

### Step 3
- In another div tag:
    - Create an ``<img>`` tag and get the `mystery.jpg` from the images folder.
    - Set the alt to mystery.
    - Create a ``<p>`` tag then copy and paste the following:
    ```plaintext
    Enter the world of cobblestone streets, candlelit mansions, and peculiar characters, where a shocking crime shakes Victorian high society. A dashing yet delightfully unconventional detective must piece together the puzzle, navigating a cast of absurd suspects and hilariously bizarre clues.
    ```
    - Create a ``<button>`` tag with an onclick event then copy and paste the following in the button tag:
    ```plaintext
    Generate Mystery Story!
    ```
<details>
<summary>Step 3 Solution</summary>

```html
<div class="category">
    <img src="images/mystery.jpg" alt="mystery">
    <p>Enter the world of cobblestone streets, candlelit mansions, and peculiar characters, where a shocking crime shakes Victorian high society. A dashing yet delightfully unconventional detective must piece together the puzzle, navigating a cast of absurd suspects and hilariously bizarre clues.</p>
    <button onclick="">Generate Mystery Story!</button>
</div>
```
</details>

### Step 4
- In the last div tag:
    - Do the same thing and get the `time_travel.jpg` from the images folder.
    - Set the alt to travel.
    - Copy and paste the following:
    ```plaintext
    Your malfunctioning time machine has created total chaos in the space-time continuum! Someone has used it to steal your homework before it was even due. It is up to you to travel through time and get it back before the bell rings for class.
    ```
    - Create a ``<button>`` tag with onclick then copy and paste the following:
    ```plaintext
    Generate Time Travel Story!
    ```

<details>
<summary> Step 4 Solution </summary>

```html
<div class="category">
    <img src="images/time_travel.jpg" alt="travel">
    <p>Your malfunctioning time machine has created total chaos in the space-time continuum! Someone has used it to steal your homework before it was even due. It is up to you to travel through time and get it back before the bell rings for class.</p>
    <button onclick="">Generate Time Travel Story!</button>
</div>
```
</details>

### Step 5
- Outside that div tag with the class category create a ``<h1>`` tag and paste in the following:
```plaintext
Your Generated Story
```
- Lastly, create a div tag with an id of output. You can leave it blank for now.

<details>
<summary>Step 5 Solution</summary>

```html
<h1>Your Generated Story</h1>
<div id="output"></div>
```

</details>

> [!NOTE]
> Everything should be inside the div tag with class `container`!

## Part II: CSS
For now your website will look kind of funky with big images and text not aligning properly.

### Step 6
In `style.css` we want the header's (the ``<h1>`` and ``<h2>`` tags) to be in the center of our website (Hint: Use Flexbox!).
  
<details>
<summary> Step 6 Solution </summary>

```css
h1, h2 {
    display: flex;
    justify-content: center;
}
```
</details>

### Step 7
Alright the images are way to big, we need to resize it. 
> [!NOTE]
> To change the style of all the images you can call the img tag (similar to the h1 and h2 tags). From there you can modify it's size, radius, transparency, etc. Overall this is what it should look like in CSS:
```css
img {
  width: 200px;
  padding: 10px;
  opacity: 0.5; /* Image transparency with a image at 50% opacity */
}
```
- Style all images to have the following:
  - `width` of 100%
  - `height` set to auto. You can just type `auto`.
  - `border-radius` to about 25 pixels.
      - This will round the corners for images.
  - `margin-bottom` to about 10 pixels. 
      - This will help space between the images and text.

<details>
<summary> Step 7 Solution </summary>

```css
img {
  width: 100%; 
  height: auto; 
  border-radius: 25px; 
  margin-bottom: 10px; 
}
```
</details>

### Step 8
- Style all paragraphs ``<p>`` to have the following:
    - `font-size` of 16 pixels.
    - `line-height` of 1.5.

<details>
<summary> Step 8 Solution </summary>

```css
p {
    font-size: 16px; 
    line-height: 1.5; 
}
```
</details>

### Step 9
- Style all buttons ``<button>`` to have the following:
    - `padding` of 10 pixels.

<details>
<summary> Step 9 Solution </summary>

```css
button {
    padding: 10px;
}
```
</details>

### ---- Feel free to change any of the values or add additional styling elements! ----

After all that, your website should look similar to this:

![demo](demo.jpg)

## Part III: JavaScript
In the `script.js` you will implement 3 functions that will be added to the onclick event in the `index.html` file.

### Step 10
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
> [!TIP]
> It is common practice to have "good" variable names related to what the variable is doing. Here is an example:
```js
var name = "Kai"; //a good variable name
console.log("Hello " + name + "!"); //we know that this greets the user with their name
// -------------------- \\
var z = "Josh"; //a bad variable name
console.log("How are you " + z + "?"); //what is z suppose to mean? Is it suppose to be a name, a continuation of a statement, an object?
```

<details>
<summary> Step 10 Solution </summary>

```js
function dinner()
{
  //it does not have to be the same variable name nor prompt
  const food = prompt("Food");
  const smthStrange = prompt ("Something Strange");
  const adj = prompt("Adjective");
  const animal = prompt("Animal");
  const verb = prompt("Verb ending in -ing");
  const obj = prompt("Object");
  const funQuote1 = prompt("A Funny Quote");
  const funQuote2 = prompt("Another Funny Quote");

}
```
</details>


### Step 11
Next we need to ensure that the user has inputted something in all of the 8 variables. We will use `if` and `else` statements. Here is the format of `if` and `else` statements in JavaScript:
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

<details>
<summary> Step 11 Solution </summary>

```js
//assuming the variables are the same in step 9
if (food && smthStrange && adj && animal && verb && obj && funQuote1 && funQuote2)
{
    //--- implement in step 12 ---\\
}
else
{
    //--- implement in step 12 ---\\
}
```
</details>

### Step 12
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

<details>
<summary>Step 12 Solution</summary>

```js
if (food && smthStrange && adj && animal && verb && obj && funQuote1 && funQuote2)
{
    document.getElementById("output").innerHTML = `
    <p>The dinner party started with a dish of ${food} that smelled like ${smthStrange}. 
    Suddenly, a ${adj} ${animal} appeared and started ${verb} on the table! 
    The host grabbed a ${obj} and yelled "${funQuote1}!" 
    We all laughed and said "${funQuote2}." It was unforgettable!</p>
    `;
}
else
{
    alert("Oops! You missed one or more inputs. Please try again!");
}
```
</details>

### Once you got this down, doing the next 2 functions will be fairly easy.

### Step 13
- Create a function named `mystery` with no parameters.
- Create 11 variables that prompts the users to enter the following (in parentheses) from this story:

```plaintext
On a(n) (ADJECTIVE) night in the grand (PLACE), a loud (SOUND) revealed Lord (SILLY NAME 1) lying beside a (OBJECT), muttering, "It was the (NOUN)!"
Detective (NAME), questioned the (JOB TITLE), who was caught (VERB) near the scene. But the truth was stranger than fiction.
It turns out Lord (SILLY NAME 1) had slipped on (SUBSTANCE) while trying to steal a plate of (FOOD).
Everyone laughed, and the detective vowed to investigate only serious cases from now on.
```

<details>
<summary>Step 13 Solution</summary>

```js
//it does not have to be the same variable name nor prompt
function mystery()
{
  const adj = prompt("Adjective");
  const place = prompt("Place");
  const sound = prompt("Sound");
  const silName = prompt("A Silly Name");
  const obj = prompt("An Object");
  const noun = prompt("A Noun");
  const name = prompt("A Name");
  const jobTitle = prompt("A Job Title");
  const verb = prompt("Verb Ending in -ing");
  const sub = prompt("A Substance");
  const food = prompt("Food");
}
```
</details>

### Step 14
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

<details>
<summary>Step 14 Solution</summary>

```js
//assuming the variables are the same in step 15
if (adj && place && sound && silName && obj && noun && name && jobTitle && verb && sub && food)
{
    document.getElementById("output").innerHTML = `
    <p>On a(n) ${adj} night in the grand ${place}, a loud ${sound} revealed Lord ${silName} lying beside a ${obj}, muttering, "It was the ${noun}!"
    Detective ${name}, questioned the ${jobTitle}, who was caught ${verb} near the scene. But the truth was stranger than fiction.
    It turns out Lord ${silName} had slipped on ${sub} while trying to steal a plate of ${food}.
    Everyone laughed, and the detective vowed to investigate only serious cases from now on.</p>
    `;
}
else
{
    alert("Oops! You missed one or more inputs. Please try again!");
}
```
</details>

### Step 15
- Lastly create a function named `travel` with no parameters.
- Create 9 variables that prompts the users to enter the following (in parentheses) from this story:

```plaintext
Your time machine malfunctions, and a (HISTORICAL FIGURE) steals your homework escaping to (PLACE)!
Armed with a (OBJECT), you chase them through time, dodging (PLURAL NOUN) and a (ADJECTIVE 1) dinosaur trying to (VERB) you.
You finally catch the thief at (EVENT IN TIME) and grab your homework just time.
Back in class, your teacher, (SILLY NAME), says, "That's the most (ADJECTIVE 2) excuse ever!" But hey, you got an A!
```

<details>
<summary>Step 15 Solution</summary>

```js
function travel()
{
  //it does not have to be the same variable name nor prompt
  const histFig = prompt("A Historical Figure");
  const place = prompt("A Place in Time");
  const obj = prompt("A Object");
  const pluNoun = prompt("A Plural Noun");
  const adj1 = prompt("Adjective");
  const verb = prompt("Verb");
  const event = prompt("An Event in History");
  const silName = prompt("A Silly Name");
  const adj2 = prompt("Adjective");
}
```
</details>

### Step 16
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

<details>
<summary>Step 16 Solution</summary>

```js
//assuming the variables are the same in step 13
if (histFig && place && obj && pluNoun && adj1 && verb && event && silName && adj2)
{
    document.getElementById("output").innerHTML = `
    <p>Your time machine malfunctions, and a ${histFig} steals your homework escaping to ${place}!
    Armed with a ${obj}, you chase them through time, dodging ${pluNoun} and a ${adj1} dinosaur trying to ${verb} you.
    You finally catch the thief at ${event} and grab your homework just time.
    Back in class, your teacher, ${silName}, says, "That's the most ${adj2} excuse ever!" But hey, you got an A!</p>
    `;
}
else
{
    alert("Oops! You missed one or more inputs. Please try again!");
}
```
</details>

## Part IV: Linking
### Step 17
- Remember [step 2](#step-2), [step 3](#step-3), and [step 4](#step-4) where you were told to leave button tags with the onclick event blank? Now go back to the `index.html` file and fill in the onclick event with your functions `dinner()`, `mystery()`, and `travel()` by putting these functions inside the quotation marks within the `onclick` events.
- Here is a reminder of the button tag in HTML:
```html
<!-- button tag -->
<button onclick="function()">Text goes here</button>
```
> [!NOTE]
> Make sure the functions are in your respective div category. For instance your `dinner()` function should be in the div tag with your dinner image, dinner description and the button that says to generate your dinner story.
- Check that everything works by pressing the buttons, entering user input, leaving inputs blank, etc.
- Your outputted story with user input will be displayed below at the bottom of the page.

<details>
<summary>Step 17 Solution</summary>

```html
<!-- in the button tags -->
<button onclick="dinner()">Generate Dinner Story!</button>
<button onclick="mystery()">Generate Mystery Story!</button>
<button onclick="travel()">Generate Time Travel Story!</button>
```
</details>

## Conclusion
Congratulations! You just created a simple Mad Libs game using functions from JavaScript to make it interactive with the user when they click a button and entering input from which it displays a humorous story based on input. 

You were able to:
- [ ] Understand the basics of div tags in HTML.
- [ ] How the button tags work.
- [ ] Review CSS Flexbox.
- [ ] JavaScript variables.
- [ ] JavaScript functions.
- [ ] If and Else statements.
- [ ] The AND operator.

For a little something extra you could make the stories longer by adding more variables and modifying the overall story to make it even more funnier. You can do this by simplily changing the text in the if statements in [step 12](#step-12), [step 14](#step-14), and [step 16](#step-16).

