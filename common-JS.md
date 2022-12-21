#COMMON JAVASCRIPT BITS

#Declaring a variable in JavaScript:

The var keyword is used to declare a variable in JavaScript. The let keyword was introduced in ECMAScript 6 (ES6) and is used to declare a block-scoped variable. The const keyword is also introduced in ES6 and is used to declare a read-only variable.

    // Declaring a variable using the var keyword
    var myVariable;

    // Declaring a variable using the let keyword
    let myVariable;

    // Declaring a variable using the const keyword
    const myVariable;

#Creating a function in JavaScript:

There are several ways to declare a function in JavaScript. The first example shows the traditional way of declaring a function using the function keyword. The second example shows a function expression, where a function is assigned to a variable. The third example shows an arrow function, which is a concise way of defining a function.

    // Declaring a function using the function keyword
    function myFunction() {
    // function body
    }

    // Declaring a function using the function expression
    const myFunction = function() {
    // function body
    };

    // Declaring a function using the arrow function notation
    const myFunction = () => {
    // function body
    };

#Using loops in JavaScript:

There are several types of loops in JavaScript that you can use to execute a block of code multiple times. The for loop is used to iterate over a range of values. The while loop is used to repeat a block of code while a certain condition is true. The do-while loop is similar to the while loop, but it always executes the block of code at least once before checking the condition.

    // Using a for loop
    for (let i = 0; i < 5; i++) {
    console.log(i);
    }

    // Using a while loop
    let i = 0;
    while (i < 5) {
    console.log(i);
    i++;
    }

    // Using a do-while loop
    let i = 0;
    do {
    console.log(i);
    i++;
    } while (i < 5);


//Using conditional statements in JavaScript:

    const x = 10;

    // Using an if statement
    if (x > 5) {
    console.log("x is greater than 5");
    }

    // Using an if-else statement
    if (x > 5) {
    console.log("x is greater than 5");
    } else {
    console.log("x is not greater than 5");
    }

    // Using an if-else if-else statement
    if (x > 15) {
    console.log("x is greater than 15");
    } else if (x > 5) {
    console.log("x is greater than 5");
    } else {
    console.log("x is not greater than 5");
    }

    // Using a switch statement
    switch (x) {
    case 10:
        console.log("x is 10");
        break;
    case 15:
        console.log("x is 15");
        break;
    default:
        console.log("x is something else");
    }

#Handling events in JavaScript:

In JavaScript, you can use the addEventListener method or the onclick property to attach an event listener to an element. An event listener is a function that is called when a specific event, such as a click event, occurs on an element.

    const button = document.querySelector("button");

    // Adding an event listener using the addEventListener method
    button.addEventListener("click", function() {
    console.log("Button was clicked!");
    });

    // Adding an event listener using the onclick property
    button.onclick = function() {
    console.log("Button was clicked!");
    };

#How do I access and manipulate the DOM in JavaScript?

To access and manipulate the Document Object Model (DOM) in JavaScript, you can use the document object and various methods and properties it provides. For example, you can use the getElementById method to access an element with a specific ID, and then use the innerHTML property to modify its content.

    <div id="myDiv">Hello World!</div>

    <script>
    // Access the div element
    var myDiv = document.getElementById("myDiv");

    // Modify its content
    myDiv.innerHTML = "New content!";
    </script>

You can also use the querySelector and querySelectorAll methods to access elements using CSS selectors, and the createElement method to create new elements. For example:

    <ul id="myList">
    <li>Item 1</li>
    <li>Item 2</li>
    </ul>

    <script>
    // Access the list element
    var myList = document.getElementById("myList");

    // Create a new list item
    var newItem = document.createElement("li");
    newItem.innerHTML = "Item 3";

    // Add the new item to the list
    myList.appendChild(newItem);

There are many other methods and properties available for accessing and manipulating the DOM, such as classList, style, setAttribute, and addEventListener. You can find more information in the documentation for the document object: https://developer.mozilla.org/en-US/docs/Web/API/Document

#How do I handle errors and exceptions in JavaScript?

To handle errors and exceptions in JavaScript, you can use the try and catch statements. The try statement allows you to specify a block of code that might throw an error, and the catch statement allows you to handle the error if it occurs. For example:

    try {
        // Code that might throw an error
        undefinedFunction();
    } catch (error) {
        // Handle the error
        console.log(error);
    }

You can also use the finally statement to specify a block of code that should be executed regardless of whether an error occurs. For example:

    try {
    // Code that might throw an error
    undefinedFunction();
    } catch (error) {
    // Handle the error
    console.log(error);
    } finally {
    // Code that should always be executed
    console.log("Finally block executed");
    }

In addition to the try and catch statements, you can also use the throw statement to throw custom errors. For example:

    function divide(a, b) {
    if (b === 0) {
        throw new Error("Cannot divide by zero");
    }
    return a / b;
    }

    try {
    var result = divide(5, 0);
    } catch (error) {
    console.log(error);
    }
  
For more information, you can check out the documentation for the try and catch statements:

#How do I use objects and arrays in JavaScript?

Objects in JavaScript are a collection of key-value pairs. You can create an object using the object literal syntax, like this:

    const person = {
        name: 'John',
        age: 30
    };

You can access the values of an object using dot notation or bracket notation. For example:

    console.log(person.name); // Output: 'John'
    console.log(person['age']); // Output: 30

You can also add, update, and delete properties of an object like this:

    person.email = 'john@example.com'; // Add a new property
    person.age = 31; // Update a property
    delete person.email; // Delete a property

Arrays in JavaScript are ordered collections of values. You can create an array using the array literal syntax, like this:

    const numbers = [1, 2, 3, 4, 5];

You can access the values of an array using index notation. For example:

    console.log(numbers[0]); // Output: 1
    console.log(numbers[4]); // Output: 5

You can also use array methods like push, pop, shift, and unshift to add and remove elements from the beginning or end of an array.

#How do I use regular expressions in JavaScript?

Regular expressions are patterns used to match character combinations in strings. You can create a regular expression in JavaScript using the RegExp constructor or the regular expression literal syntax, like this:

    const regex1 = new RegExp('abc');
    const regex2 = /abc/;

You can use the test method of a regular expression to test if a string matches the pattern. For example:

    console.log(regex1.test('abcdef')); // Output: true
    console.log(regex1.test('abxdef')); // Output: false

You can use the exec method of a regular expression to get more information about the match. For example:

    const result = regex1.exec('abcdef');
    console.log(result[0]); // Output: 'abc'

You can also use special characters in regular expressions to match certain types of characters. For example:

    const regex3 = /\d/; // Match any digit
    const regex4 = /\w/; // Match any word character (alphanumeric)
    const regex5 = /\s/; // Match any whitespace character

#How do I use the fetch API to make HTTP requests in JavaScript?

The fetch API is a modern way to make HTTP requests in JavaScript. You can use it to send GET, POST, PUT, DELETE, and other types of requests.

To use the fetch API to make an HTTP request in JavaScript, you can call the fetch function and pass it the URL of the request as the first argument. For example, to send a GET request to the URL https://api.example.com/endpoint, you can do this:

    fetch('https://api.example.com/endpoint')
    .then(response => {
        // Do something with the response here
    })
    .catch(error => {
        // Handle any errors here
    });

The fetch function returns a promise that resolves with a Response object. You can use the then method of the promise to specify a callback function that will be called when the response is received.

Inside the callback function, you can access the response data using the json method of the Response object, like this:

    fetch('https://api.example.com/endpoint')
    .then(response => response.json())
    .then(data => {
    // Do something with the data here
    })
    .catch(error => {
    // Handle any errors here
    });

The json method also returns a promise that resolves with the parsed JSON data. You can use the then method of this promise to access the data.

You can also use the fetch function to send other types of requests, such as POST, PUT, DELETE, etc. To do this, you can pass an options object as the second argument to fetch, like this:

    const options = {
        method: 'POST', // POST, PUT, DELETE, etc.
        body: JSON.stringify({key: 'value'}), // Request body
        headers: {
        'Content-Type': 'application/json'
        }
    };
    
    fetch('https://api.example.com/endpoint', options)
    .then(response => response.json())
    .then(data => {
        // Do something with the data here
    })
    .catch(error => {
        // Handle any errors here
    });