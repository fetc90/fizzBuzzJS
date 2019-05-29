## Learning Objectives covered
---

JavaScript is a scripting language built for the web, and is the main language of the web as it is used by 75% of websites. This is because it is the only language that can be executed in the browser.
It doesn't have to make requests to a server the same way html does, which means it can be used for building interactivity within one page.

Use the Chrome console as a REPL
- Right click on web page > Inspect
- Click on console

```
console.log("Hello, world")
Hello, world
```

Understand JavaScript language conventions.
- The function keyword in JavaScript creates an object that can be invoked.
- If you want to return a value from a JavaScript function, you must explicitly use return, otherwise it will just return undefined.
- You must include the parentheses when invoking a function, even if there are no arguments.

Here we create a function that takes one parameter.

```
hi = function(name) {return 'Hi ' + name;}

hi('turtle')
"Hi turtle"
```

Here we created an empty object and gave it a function we can invoke with one parameter.

```
greeting = {}
greeting.hello = function(name) { return name; }

greeting.hello('n00bs');
"n00bs"

greeting.hello = function(name) { return 'hello' + name; }

greeting.hello(' Nick');
"hello Nick"
```

- We know that joining two arrays together automatically becomes a string with no spaces.

```
mix = ['hat', 4, 7]
hat = 'hat'
array = [hat, hat, hat]

array + mix
"hat,hat,hathat,4,7"
```
Blank object can have their own variables.

```
door = {}
door.handle = 'metal'
door.handle
"metal"
door
{handle: "metal"}

```

Loops

Here we make a for loop that prints the numbers 1 to 10 in the browser console:

```
for (x = 0; x < 11; x++) {console.log(x)}
```

Prints the numbers 1 to 5:

```
var i = 0;
do {
  i += 1;
  console.log(i);
} while (i < 5);

```

Checks if two variables are the same:

```
1 === 1
true
```

## Our Approach
---
We broke the pairing session down into 25 minute sections, clarifying what we wanted to achieve in each block.

![25_mins](./images/25_mins.jpg)


## First Error message
---

Writing our first TDD test with Jasmin and running the file in browser.


![first_error](./images/first_error.png)

Passing first error message:

< fizzBuzzSpec.js >

```
describe('Javabuzz',function() {

var javabuzz;

  describe('knows when a number is', function() {

    it('divisible by 3',function() {
        javabuzz = new Javabuzz();
        expect(javabuzz.isDivisibleByThree(3)).toBe(true);
    });

  });

});
```

in fizzBuzz.js file

```
var Javabuzz = function(){};

Javabuzz.prototype.isDivisibleByThree = function (number) {
  return true;
};

```

![first_error_fix](./images/first_error_fix.png)
