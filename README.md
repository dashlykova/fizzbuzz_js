```
Question 1. In your README to the best of your knowledge please explain what the following lines of code do

global.browser = new BrowserHelpers()
global.expect = chai.expect;

Answer 1.
We are basically telling how we want the tests to run.

global.browser = new BrowserHelpers()
Any browser that will run our program will use Browser Helpers

global.expect = chai.expect;
Chai is a BDD/TDD assertion library that can be paired with any JS testing framework. It provides us the status(failures) of the tests in a natural language and in a expressive, readable style.
Since we have earlier required chai in our spec.helper file, global will install chai at (redudantly) global level, which means that it expects chai to run the tests throughout the command line.
```
```
Question 2. In your README to the best of your knowledge please explain why we are placing the let fizzBuzz = new FizzBuzz outside the it block?

Answer 2.
Because we want a new instance of fizzbuzz to run through each test, instead of having the tests run through the same instance every time.
```
```
Question 3. In your README to the best of your knowledge please explain the difference between using === and == in JS?

=== demands complete equality in type and value of what we are passing
Example: 'Dash' === 'Dash' (both are strings and have the same value)
9 === 9 (both are integers and have the same value)

== is more or less equal
Example: 9 == '9'
```
```
Question 4. In your README to the best of your knowledge please explain why we are moving (number % 5 === 0) to the top?

Answer 4.
Because JS reads the code from top to bottom, hierarchically.
```
```
Question 5. In your README to the best of your knowledge please explain the difference between feature and unit test

Answer 5.

Unit test => is a test you run for a specific piece of code. Unit testing is implemented when we want to test the smallest piece of code to check whether it's fit for use.

Feature test (or acceptance test, as it's also called) => is much broader testing of the scenarios that a user would face while interacting with our app. It's much more detailed and has a happy path(when the user does exactly what we want him to do and follows the instructions to the letter. Which, obvs never happens!) and a sad path (this where the user is being a bit of a rebel and refuses to even spell their names right)
```
```
Question 6. In your README to the best of your knowledge please explain what this following code does

describe('User can input a value and get FizzBuzz results', () => {
    before(async () => {
        await  browser.init()
        await  browser.visitPage('http://localhost:8080/')
    });

    beforeEach(async () => {
        await  browser.page.reload();
    })

    after(async ()=> {
        await  browser.close();
    })
})

Answer 6.
I am telling/describing the program what I want it to do. In this case, I am telling it that I want a user(person) to give me/write a number (value) and get the result for our FizzBuzz game. 
I am taking advantage of the asynchronous property of the programming language, which is based on a promise, so that all of the commands that I pass won't have to run simultaniously.
Await expression in the async function pauses the execution of the function and waits for the passed
promise's resolution, and then resumes the async function's execution and returns the resolved value. 
```
```
Question 7. In your README to the best of your knowledge please explain what expectations in the context of testing are:

it('clicking on the "Check" button', async () => {
    await browser.fillIn("input[id='value']", { with:  "3" })
    await browser.clickOnButton("input[value='Check']")
    let content = await browser.getContent("[id='display_answer']")
    expect(content).to.eql('Fizz');
})

Answer 7.
It is expected that the user will click on the "Check" button and type 3.
Upon the click of the button the program will get the content of the answer and display it.
The expected content value has to be equal to "Fizz"
```
```
Question 8. In your README to the best of your knowledge please write a line to line explanation of what is happening in this code

<script src="js/fizzbuzz.js"></script>  //=> Connecting JS file in src/js folder to our HTML file 

    <script>
        document.addEventListener('DOMContentLoaded', () => { //=> Adding the event listener to our web 
        apllication. Event listener pays attention to whatever event occurs. We are connecting our JS code to the DOM, which allows us to manipulate the HTML.

            let button = document.getElementById('button') => Creating a variable called "button" and connecting it to an HTML element with an ID name "button"

            let displayDiv = document.getElementById('display_answer') => when clicking the button, an answe should be displayed

            button.addEventListener('click', () =>{ => Upon the click
                let value = document.getElementById('value').value => get the value of the typed in number
                let fizzBuzz = new FizzBuzz => Create a new instance of FizzBuzz and put it in to variable fizzBuzz
                let result = fizzBuzz.check(value) => checking the value of the result
                displayDiv.innerHTML = result; => displaying the result
            })
        })
    </script>
```
```
Question 9. In your README to the best of your knowledge please explain what a CDN (Content Delivery Network) is?

Answer 9.
A CDN is a system of servers that deliver pages and web content to users, based on geographic locations of the users.
```
