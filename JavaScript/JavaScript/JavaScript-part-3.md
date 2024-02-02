[JavaScript part 0](JavaScript/JavaScript-part-0.md) / [JavaScript part 3](#)



# JavaScript Part 3

# DOM (Document Object Model)

## Getting Element

We can access already created element or elements using JavaScript. To access or get elements we use different methods. 

### Getting elements by tag name

***`getElementsByTagName()`***:takes a tag name as a string parameter and this method returns an HTMLCollection object. 

An HTMLCollection is an array like object of HTML elements. 

The length property provides the size of the collection. Whenever we use this method we access the individual elements using index or after loop through each individual items. 

An HTMLCollection does not support all array methods therefore we should use regular for loop instead of `forEach`.

```jsx
// syntax
document.getElementsByTagName('tagname')
```

```jsx
const allTitles = document.getElementsByTagName('h1')

console.log(allTitles) //HTMLCollections
console.log(allTitles.length) // 4

for (let i = 0; i < allTitles.length; i++) {
  console.log(allTitles[i]) // prints each elements in the HTMLCollection
}
```

### Getting elements by class name

***`getElementsByClassName()`*** method returns an HTMLCollection object. An HTMLCollection is an array like list of HTML elements. The length property provides the size of the collection. It is possible to loop through all the HTMLCollection elements. See the example below

```jsx
//syntax
document.getElementsByClassName('classname')
```

```jsx
const allTitles = document.getElementsByClassName('title')

console.log(allTitles) //HTMLCollections
console.log(allTitles.length) // 4

for (let i = 0; i < allTitles.length; i++) {
  console.log(allTitles[i]) // prints each elements in the HTMLCollection
}
```

### Getting an element by id

***`getElementsById()`*** targets a single HTML element. We pass the id without # as an argument.

```jsx
//syntax
document.getElementById('id')
```

```jsx
let firstTitle = document.getElementById('first-title')
console.log(firstTitle) // <h1>First Title</h1>
```

### Getting elements by using `querySelector` methods

The *`document.querySelector`* method can select an HTML or HTML elements by tag name, by id or by class name.

***`querySelector`***: can be used to select HTML element by its tag name, id or class. If the tag name is used it selects only the first element.

```jsx
let firstTitle = document.querySelector('h1') // select the first available h1 element
let firstTitle = document.querySelector('#first-title') // select id with first-title
let firstTitle = document.querySelector('.title') // select the first available element with class title
```

***`querySelectorAll`***: can be used to select html elements by its tag name or class. It returns a nodeList 

nodeList  is an array like object which supports array methods. We can use ***for loop*** or ***forEach*** to loop through each nodeList elements.

```jsx
const allTitles = document.querySelectorAll('h1')// # selects all the available h1 elements in the page

console.log(allTitles.length) // 4
for (let i = 0; i < allTitles.length; i++) {
  console.log(allTitles[i])
}

allTitles.forEach(title => console.log(title))
const allTitles = document.querySelectorAll('.title') // the same goes for selecting using class
```

## Manipulating attributes

### Adding Text to HTML element

An HTML is a build block of an opening tag, a closing tag and a text content. We can add a text content using the property *textContent* or *innerHTML.

### Adding Text content using textContent

The *textContent* property is used to add text to an HTML element.

```jsx
const titles = document.querySelectorAll('h1')
titles[3].textContent = 'Fourth Title'
```

### Adding Text Content using innerHTML

Most people get confused between *textContent* and *innerHTML*. *textContent* is meant to add text to an HTML element, however innerHTML can add a text or HTML element or elements as a child.

### Text Content

We assign *textContent* HTML object property to a text

```
const titles = document.querySelectorAll('h1')
titles[3].textContent = 'Fourth Title'
```

### Inner HTML

We use `innerHTML` property when we like to replace or a completely new children content to a parent element. It value we assign is going to be a string of HTML elements.

```jsx
<!DOCTYPE html><html lang="en">
  <head>
    <title>JavaScript for Everyone:DOM</title>
  </head>
  <body>
    <div class="wrapper">
        <h1>Asabeneh Yetayeh challenges in 2020</h1>
        <h2>30DaysOfJavaScript Challenge</h2>
        <ul></ul>
    </div>
    <script>
	    const lists = `
		    <li>30DaysOfPython Challenge Done</li>
		    <li>30DaysOfJavaScript Challenge Ongoing</li>
		    <li>30DaysOfReact Challenge Coming</li>
		    <li>30DaysOfFullStack Challenge Coming</li>
		    <li>30DaysOfDataAnalysis Challenge Coming</li>
		    <li>30DaysOfReactNative Challenge Coming</li>
		    <li>30DaysOfMachineLearning Challenge Coming</li>
			`
		  const ul = document.querySelector('ul')
		  ul.innerHTML = lists
			//ul.innerHTML = lists this would empty the element
    </script>
  </body>
</html>
```

### Adding style

```jsx
const titles = document.querySelectorAll('h1')
titles.forEach((title, i) => {
  title.style.fontSize = '24px' // all titles will have 24px font size
  if (i % 2 === 0) {
    title.style.color = 'green'
  } else {
    title.style.color = 'red'
  }
})
```

```jsx
const allTitles = document.getElementsByClassName('title')

allTitiles.className = "new-class-name"
allTitiles.id = "new-id"
allTitles0[i].setAttribute("style", "color:red;") //to manipulate any atrribute

```

### Adding new elements

```jsx
<!DOCTYPE html>
<html lang="en">

<head>
  <title>Document Object Model</title>
</head>

<body>
  <h2>person</h2>
  <ul>
    <li>Kidanu</li>
    <li>Bekele</li>
  </ul>

  <script>
    let peopleList = ["Abebe", "Chala", "Bekele", "Tirsit"]
    let ulList = document.querySelector("ul")
    peopleList.forEach((value, index, arr) => {
      let listElement = document.createElement("li")
      listElement.textContent = value;
      ulList.appendChild(listElement);

      console.log(value);

    })
  </script>

</body>

</html>
```

# Promise

A Promise is a way to handle asynchronous operations in JavaScript. It allows handlers with an asynchronous action's eventual success value or failure reason. This lets asynchronous methods return values like synchronous methods: instead of immediately returning the final value, the asynchronous method returns a promise to supply the value at some point in the future.

A Promise is in one of these states:

- pending: initial state, neither fulfilled nor rejected.
- fulfilled: meaning that the operation completed successfully.
- rejected: meaning that the operation failed.
