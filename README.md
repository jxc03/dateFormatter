<h1 align="center">
  Date Formatter
</h1>

<p>
  In this project, I learn how to work with JavaScript Date object including its methods and properties as well as how to correctly format dates. This project covered conceps such as the <b>getDate()</b>, <b>getMonth()</b> and <b>getFullYear()</b> methods. 
</p>

## Preview


## Steps
**S1**<br>
In this project, you will learn about the JavaScript `Date` object by building a date formatter.<br>
All of the HTML and CSS for this project have been provided for you.<br>
Start by getting the `#current-date` element using the `.getElementById()` method and assign it to a `const` variable called `currentDateParagraph`.

```js
const currentDateParagraph = document.getElementById("current-date"); 
```

**S2**<br>
Use the `.getElementById()` method to get the `#date-options` element and use `const` to assign it to a variable named `dateOptionsSelectElement`.

```js
const dateOptionsSelectElement = document.getElementById("date-options");
```

**S3**<br>
In JavaScript, there are many built-in <i>constructors</i> that create objects. A constructor is like a regular function, but starts with a capital letter, and is initialized with the `new` operator.<br>
For example, you can use the `Date()` constructor with the `new` operator to create a new `Date` object that returns a string with the current date and time:<br>
<b>Example Code</b>
`const currentDate = new Date();`<br>
`console.log(currentDate);`<br>
`// Output:`<br>
`// Mon Aug 23 2021 15:31:00 GMT-0400 (Eastern Daylight Time)`<br>
Create a new `const` variable called `date` and assign it a `Date` object with `new Date()`.

```js
const date = new Date();
```

**S4**<br>
The `Date` object has a number of methods that allow you to get the date and time in different formats.<br>
One of those is the `.getDate()` method, which returns a number between `1` and `31` that represents the day of the month for that date. For example:<br>
<b>Example Code</b><br>
`const date = new Date();`<br>
`const dayOfTheMonth = date.getDate();`<br>
`console.log(dayOfTheMonth); // 20`<br>
Using `const`, create a variable named `day` and assign it the day of the month from `date` with the `.getDate()` method.

```js
const day = date.getDate();
```

**S5**<br>
The `.getMonth()` method returns a number between `0` and `11`. This represents the month for the date provided, where `0` is January and `11` is December. Because the number this method returns is zero-based, you need to add `1` to it to get the expected month number.<br>
Using `const`, create a variable named `month` and assign it the month from `date` with the `.getMonth()` method.<br>
Remember to add `1` to the number returned by `.getMonth()`.

```js
const month = date.getMonth() + 1;
```

**S6**<br>
The `.getFullYear()` method returns a number which represents the year for the provided date.<br>
Using `const`, create a variable named `year` and assign it the year from `date` with the `.getFullYear()` method.

```js
const year = date.getFullYear();
```

**S7**<br>
The `.getHours()` method returns a number between `0` and `23`. This represents the hour for the provided date, where `0` is midnight and `23` is 11 p.m.<br>
Create a `const` variable named `hours` and assign it the hour from `date` with the `.getHours()` method.

```js
const hours = date.getHours();
```

**S8**<br>
The `.getMinutes()` method returns a number between `0` and `59` which represents the minutes for the provided date.<br>
Create a `const` variable named `minutes` and assign it the minutes from `date` with the `.getMinutes()` method.

```js
const minutes = date.getMinutes();
```

**S9**<br>
Next, create a `const` variable named `formattedDate` and assign it empty template literals.

```js
const formattedDate = ``;
```

**S10**<br>
Inside the template literal, add an embedded expression that contains the `day` variable.

```js
const formattedDate = `${day}`;
```

**S11**<br>
After the `day` variable, add a dash (`-`) followed by another embedded expression that contains the month variable.

```js
const formattedDate = `${day}-${month}`;
```

**S12**<br>
After the `month` variable, add a dash followed by another embedded expression that contains the `year` variable.

```js
const formattedDate = `${day}-${month}-${year}`;
```

**S13**<br>
To see the results of the `formattedDate` variable, add a `console.log()` statement and pass in the `formattedDate` variable as an argument.<br>
Open up the console and you should see the date printed out.

```js
console.log(formattedDate)
```

**S14**<br>
Use the `textContent` property on `currentDateParagraph` to set its text content to the value of the `formattedDate` variable.<br>
Also, make sure to remove your `console.log(formattedDate);` line.

```js
currentDateParagraph.textContent = formattedDate;
```

**S15**<br>
In JavaScript, the `change` event is used to detect when the value of an HTML element has changed:
Example Code<br>
`element.addEventListener("change", () => {`<br>
`});`<br>
Attach the `addEventListener` method to the `dateOptionsSelectElement`. The first argument of the event listener should be the string `"change"` and the second argument should be an empty arrow function.

```js
dateOptionsSelectElement.addEventListener("change", () => {});
```

**S16**<br>
When a user makes a selection from the dropdown menu, the function should get the user's value and display the date in their chosen date format. To do this, you can use the `switch` statement.<br>
A `switch` statement is used to compare an expression against multiple possible values and execute different code blocks based on the match. It's commonly used for branching logic.<br>
For example, here's how to compare the expression `dayOfWeek` against possible values:<br>
<b>Example Code</b><br>
`switch (dayOfWeek) {`<br>
  `case 1:`<br>
    `console.log("It's Monday!");`<br>
    `break;`<br>
  `case 2:`<br>
    `console.log("It's Tuesday!");`<br>
    `break;`<br>
  `// ...cases for other workdays`<br>
  `default:`<br>
    `console.log("It's the weekend!");`<br>
}<br>
Create a `switch` statement and use `dateOptionsSelectElement.value` as the expression.

```js
switch (dateOptionsSelectElement.value) {}
```

**S17**<br>
When the user chooses the `Year, Month, Day` option from the dropdown, the date format should reflect this choice.<br>
To do this, you can add a `case` clause in the `switch` statement that checks for a match against the expression `expr`, followed by code to run if there's a match. Here's an example where the `case` clause checks that `expr` is equal to the string `"case123"`:<br>
<b>Example Code</b><br>
`switch (expr) {`<br>
  `case 'case123':`<br>
    `// Write your logic here`<br>
`}`<br>
Add a `case` where the value is `"yyyy-mm-dd"`. Inside the `case`, set the text content of `currentDateParagraph` to the value of `formattedDate`.

```js
case "yyyy-mm-dd": 
    currentDateParagraph.textContent = formattedDate;
```

**S18**<br>
To format the date into `yyyy-mm-dd`, you will need to use the <i>split</i>, <i>reverse</i>, and <i>join</i> methods. But first, you will need to go through a few practice examples so you can better understand how to use them in the context of this project.<br>
The `split()` method is used to divide a string into substrings based on a specified separator. It then returns these substrings as elements of an array.<br>
Here is an example of taking the words `"Hello World"` and returning an array of one element:<br>
<b>Example Code</b><br>
`const greeting = "Hello World";`<br>
`greeting.split(); // ["Hello World"]`<br>
Create a new `const` variable called `exampleSentence` and assign it the result of `"selur pmaCedoCeerf".split()`.<br>
Then add a console statement to log the value of `exampleSentence`. Open up the console to see the result.

```js
const exampleSentence = "selur pmaCedoCeerf".split();
console.log(exampleSentence);
```

**S19**<br>
The `split` method takes in a parameter known as a separator. The separator is used to tell the computer where each split should occur.<br>
Here is an example of using an empty string as a separator:<br>
<b>Example Code</b><br>
`// returns ["h", "e", "l", "l", "o"]`<br>
`"hello".split("");`<br>
Other examples of separators can include a space `" "`, or a hyphen `"-"`. If you don't provide a separator, the method will return an array with the original string as the only element.<br>
Update your `split` method, to use an empty string as a separator. Open up the console again to see the result.

```js
const exampleSentence = "selur pmaCedoCeerf".split("");
```

**S20**<br>
To reverse an array of elements, you can use the `reverse` method. This method reverses the order of the elements in the array in place. The first element becomes the last, and the last element becomes the first.<br>
Here is an example of using the `reverse` method:<br>
<b>Example Code</b><br>
`// returns [5, 4, 3, 2, 1]`<br>
`[1, 2, 3, 4, 5].reverse();`<br>
Chain the `reverse` method to your `split` method. Open up the console again to see the result.<br>
Remember that you learned how to chain methods in the previous project like this:<br>
<b>Example Code</b><br>
`method1().method2().method3();`

```js
const exampleSentence = "selur pmaCedoCeerf".split("").reverse();
```

**S21**<br>
In the previous project, you learned how to work with the `join` method. This method takes an array of elements and joins them into a string. Similar to the `split` method, the `join` method also takes an optional separator. If you don't provide a separator, the default separator is a comma.<br>
Here is an example of using the `join` method:<br>
<b>Example Code</b><br>
`// returns "1-2-3-4-5"`<br>
`[1, 2, 3, 4, 5].join("-");`<br>
Chain the `join` method to your `reverse` method. Pass in an empty string as the separator.<br>
Open up the console and see the output.

```js
const exampleSentence = "selur pmaCedoCeerf".split("").reverse().join("");
```

**S22**<br>
Now that you have a better understanding on how to work with the `split`, `reverse`, and `join` methods, you can delete your `exampleSentence` variable and console statement.

```js
```

**S23**<br>
Now it is time to apply what you learned in the previous steps.<br>
Split the `formattedDate` string into an array of substrings. Use a `"-"` for the separator.

```js
currentDateParagraph.textContent = formattedDate.split("-")
```

**S24**<br>
Next, reverse the `formattedDate` array. Make sure to use method chaining.

```js
currentDateParagraph.textContent = formattedDate.split("-").reverse()
```

**S25**<br>
Finally, join the results from the array reversal. Use a `"-"` as the separator. Remember to use method chaining.<br>
Test out your changes by selecting the `Year, Month, Day` option from the dropdown menu. The date should now be displayed in the format `yyyy-mm-dd`.

```js
formattedDate.split("-").reverse().join("-")
```

**S26**<br>
If your `switch` statement is going to have multiple cases, it is best practice to include a `break` statement.<br>
The `break` statement will tell the JavaScript interpreter to stop executing statements. Without adding a `break` statement at the end of each `case` block, the program will execute the code for all matching `cases`:<br>
<b>Example Code</b><br>
`switch (someVariable) {`<br>
  `case 'case123':`<br>
    `// Write your logic here`<br>
    `break; // Terminates the switch statement`<br>
`}`<br>
Add a `break` statement to the end of your `case` block.

```js
break;
```

**S27**<br>
Add another `case` with the value `"mm-dd-yyyy-h-mm"`. Inside that `case`, set the text content of `currentDateParagraph` to empty template literals.<br>
Also, make sure to include a `break` statement to terminate the `switch` statement.

```js
case "mm-dd-yyyy-h-mm":
  currentDateParagraph.textContent = ``
break;
```

**S28**<br>
When the user selects the `Month, Day, Year, Hours, Minutes` option from the dropdown, you need to display the date in the format `mm-dd-yyyy h Hours m Minutes`.<br>
Inside the `case` for `mm-dd-yyyy-h-mm`, use string interpolation to assign the formatted date from above to the `textContent` property of `currentDateParagraph`. Make sure to use the `month`, `day`, `year`, `hours`, and `minutes` variables in your answer.

```js
currentDateParagraph.textContent = `${month}-${day}-${year} ${hours} Hours ${minutes} Minutes`;
```

**S29**<br>
In a `switch` statement, the `default` case is executed when none of the previous case conditions match the value being evaluated. It serves as a catch-all for any other possible cases. For example:<br>
<b>Example Code</b><br>
`const dayOfWeek = 7;`<br>
`switch (dayOfWeek) {`<br>
  `case 1:`<br>
    `console.log("It's Monday!");`<br>
    `break;`<br>
  `case 2:`<br>
    `console.log("It's Tuesday!");`<br>
    `break;`<br>
  `// ...cases for other workdays`<br>
  `default:`<br>
    `console.log("It's the weekend!");`<br>
`}`<br>
For the `default` case, set the text content of `currentDateParagraph` to the value of `formattedDate`.<br>
And with that, your date formatter is complete! You can now format the current date three different ways.

```js
default: 
  currentDateParagraph.textContent = formattedDate
```