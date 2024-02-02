[JavaScript](../JavaScript.md) / JavaScript part 0



# JavaScript part 0

- Node.js
    
    is a runtime environment used to run JavaScript on machine.
    

# Data Types
- ## Primitive datatypes
    - numbers: `int` and `float`
    - bool: `true` or `false`
    - string: uses single quote by convention
    
    ```cpp
    x = 12
    ```
    
    | x |  |
    | --- | --- |
    | 12 |  |
    | 004 |  |
    
    ```cpp
    y = x
    ```
    
    | x | y |
    | --- | --- |
    | 12 | 12 |
    | 004 | 005 |
    
    ```cpp
    x = 6
    ```
    
    | x | y |
    | --- | --- |
    | 6 | 12 |
    | 004 | 005 |
- ## Non primitive datatypes
    
    AKA reference data types 
    
    - Class
    - String
    - Array
    - Interface
    
    ```cpp
    names = {'Hanna', 'Abel'}
    ```
    
    | names |  |
    | --- | --- |
    | 101 |  |
    
    | Hanna | Abel |
    | --- | --- |
    | 101 | 101 |
    | 004 | 005 |
        

# Variable declaration
- ## Automatically
    
    ```jsx
    x = 5;
    y = 6;
    z = x + y;
    ```
    
- ## Using `var`
    
    The `var` keyword should only be used in code written for older browsers.
    
    ```jsx
    var x = 5;
    var y = 6;
    var z = x + y;
    ```
    
- ## Using `let`
    
    ```jsx
    let firstname = 'Hallan'
    ```
    
- ## Using `const`
    
    used to declare constant variables. These values cannot be changed.
    
    ```jsx
    const firstName = 'Hallan'
    const PI = 3.14 //by convention capital letters are used for const
    ```
        
# Operators
- ## Assignment operators
    
    
    | Operator | Description |
    | --- | --- |
    | + | Addition |
    | - | Subtraction |
    | * | Multiplication |
    | ** | Exponentiation (https://www.w3schools.com/js/js_2016.asp) |
    | / | Division |
    | % | Modulus (Division Remainder) |
    | ++ | Increment |
    | -- | Decrement |
    
- ## Ternary operator
    
    ```jsx
    //output: underage
    let age = 17
    let adult = (age >= 18) ? 'adult' : 'underage'
    console.log(adult)
    ```
        
# Array
    
a special variable, which can hold more than one value:

```jsx
const arr1 =[23, 4, 23, 4, 324, , 324, 3, 5]

console.log(arr1[6])
```
    
#  Function
- ## function with no return value
    
    ```jsx
    //output: Hello
    function greet()
    {
        console.log('Hello')
    }
    
    greet()
    ```
    
- ## function with return value
    
    ```jsx
    //output: Hello
    function greet()
    {
        return 'Hello'
    }
    console.log(greet())
    ```
    
- ## anonymous function
    
    ```jsx
    //output: Hello Hanna
    let firstName = 'Hanna'
    
    let func = function(name)
    {
        return 'Hello ' + name
    }
    console.log(func(firstName))
    ```
    
- ## arrow function
    
    ```jsx
    /*output: 
    Hello World!
    Hello World!
    */
    hello = () => {
        return "Hello World!";
    }
    console.log(hello)
    
    hello2 = () => "Hello World!";
    console.log(hello2)
    
    fName = 'Abebe'
    hello3 = (val) => "Hello " + val;
    console.log(hello3(fName))
    ```
    
    if we have only one parameter, you can skip the parentheses as well
    
    ```jsx
    //output: 30
    let a = 10
    let b = 3
    
    let myFunction = (a, b) => a * b;
    
    console.log(myFunction(a, b))
    ```


# JavaScript `string` methods

### String length

`length`

returns the length of a string

```jsx
let text = "The quick brown fox"
let length = text.length;
console.log(length)
/*logs:
9
*/
```

### String Parts

`slice(start, end)`

extracts a part of a string and returns the extracted part in a new string.

parameters: start position, and end position (EP not included)

```jsx

let text = "The quick brown fox"
let part = text.slice(0, 2);
console.log(part)
/*logs
The
*/

//one parameter means from position to the rest of the string
let text = "The quick brown fox"
let part2 = text.slice(4) 
console.log(part2)
/*logs:
quick brown fox
*/

//negative parameter means count from the end
let text = "The quick brown fox"
let part2 = text.slice(-3) 
console.log(part2)
/*logs:
fox
*/
```

`substring(start, end)`

* the same as `slice(start, end)` except

*!! negative parameters are treated as 0*

extracts a part of a string and returns the extracted part in a new string.

parameters: start position, and end position (EP not included)

`substr(start, length)`

* the same as `slice(start, end)` except

!! the second parameter specifies the length of the extracted part

```jsx

let text = "The quick brown fox"
let part = text.substr(0, 2);
console.log(part)
/*logs
Th
*/

//one parameter means from position to the rest of the string
let text = "The quick brown fox"
let part2 = text.substr(4) 
console.log(part2)
/*logs:
quick brown fox
*/

//negative parameter means count from the end
let text = "The quick brown fox"
let part2 = text.substr(-3) 
console.log(part2)
/*logs:
fox
*/
```

`split(delimiter)`

split a string into array items per specified delimiter and returns the array.

```jsx
let text = "The quick black fox"
arr = text.split(" ");
console.log("arr[1]:", arr[1])
/*logs
quick
*/

```

### Replacing content

`replace()`

replaces a specified value with another value in a string

- doesn’t change the string it is called on

```jsx

let text = "The quick brown fox"
let newText = text.replace("fox", "dog");
console.log(newText)
/*logs
The quick brown dog
*/

//to replace all matches we use /g flag
let text2 = "The quick brown fox fox"
let newText2 = text2.replace("fox", "dog");
console.log(newText)
/*logs
The quick brown dog dog
*/

```

`replaceAll()`

replaces all specified values with another value in a string

```jsx
let text = "the quick brown fox jumbed over the lazy dog"
text = text.replaceAll("the", "a");
console.log(text)
/*logs
a quick brown fox jumped over a lazy dog
*/
```

### Converting Case

`toUpperCase()`

```jsx
let text = "the quick"
text = text.toUpperCase();
console.log(text)
/*logs
THE QUCICK
*/
```

`toLowerCase()`

```jsx
let text = "The Quick"
text = text.toLowerCase();
console.log(text)
/*logs
the quick
*/
```

### Concatenation

`concat()`

joins two or more strings like the `+` operator

```jsx
let text1 = "The"
let text2 = "Quick"
let text3 = text1.concat(" ", text2);
console.log(text3)
/*logs
The Quick
*/
```

### Trimming

`trim()`

removes whitespace from both sides of string

```jsx
let text = "   The Quick "
text = text.trim();
console.log(text)
/*logs
The Quick
*/
```

`trimStart()`

* the same as `trim()`

!! only removes whitespace from the start of the string

```jsx
let text = "   The Quick  "
text = text.trimStart();
console.log(text)
/*logs
The Quick  
*/
```

`trimEnd()`

* the same as `trim()`

!! only removes whitespace from the end of the string

```jsx
let text = "   The Quick  "
text = text.trimEnd();
console.log(text)
/*logs
   The Quick
*/
```

### Searching

`indexOf()`

search and return the index of the first occurrence of argument

- if not found it will return `-1`

```jsx
let text = "The quick black fox"
position = text.indexOf("quick");
console.log(position)
/*logs
4
*/
```

`lastIndexOf()`

search and return the index of the last occurrence of a mentioned character or substring within the string.

- if not found it will return `-1`

`charAt()`

returns the character that is located at the given position in the string

```jsx
let text = "The quick black fox"
char = text.charAt(4);
console.log(char)
/*logs
q
*/
```
