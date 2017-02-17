# FizzBuzz

Using Test Driven Development to solve FizzBuzz.

## Defining the problem

Before we start, and for the ones who are not familiar with the FizzBuzz problem, the idea is to display integers from 1 to 100, but

- for multiples of 3 we will display the word **Fizz** instead of the integer,
- for multiples of 5 we will output **Buzz** instead of the integer and
- for multiples of 3 and 5 we’ll display **FizzBuzz**,

an example of the output below:
```
1
2
Fizz
4
Buzz
Fizz
```
## Defining the tool

**TDD** is basically a methodology or a software development process that is based on the repetition of the following tasks:

- write a simple test that defines an expected functionality/outcome
- make the test fail (it will fail as we haven’t written any code just yet!)
- write your code as simple as possible to make your test pass
- refactor your code and run the same test again (it should pass as even though is refactored the functionality should be the same.

> The key concept is to write your **unit test before** you write a line of implementation **code**.

## Let’s get started!

#### 1. Clone

Clone the repository by copy-pasting the following command into your terminal:
```
git clone https://github.com/skibinska/fizzbuzz.git && cd fizzbuzz
```
#### 2. Go to test/tests.js

We will start by writing the most simple unit test of all, a unit test that will output the first integer of the list:

```javascript
QUnit.test( "when 1, returns 1", function (assert) {
    assert.equal( fizzbuzz(1), 1, "Test passed: returns 1" );
 });
```
The test fails because **fizzbuzz is not defined**.

So we need to add the method to index.js file:

```javascript
function fizzbuzz () {}
```
This make the test fail too beacuse it expect **1** but got **undefined**.

Now let’s write the simplest possible code to make the test pass:

```javascript
function fizzbuzz () {
  return 1;
}
```
Yaah! The test passed! 
