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


