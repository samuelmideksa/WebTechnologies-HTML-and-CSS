# JavaScript String methods

Course: Web Technologies (https://www.notion.so/Web-Technologies-9040d79d92844804bec7c112fc8e43e6?pvs=21)
Date: December 23, 2023
Type: Assignment
Status: Completed

[JavaScript String Methods](https://www.w3schools.com/js/js_string_methods.asp)

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