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


