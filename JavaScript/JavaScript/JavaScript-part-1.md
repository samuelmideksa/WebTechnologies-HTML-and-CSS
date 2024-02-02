[JavaScript](../JavaScript.md) / [JavaScript part 1](JavaScript/JavaScript-part-1.md)



# JavaScript part 1

### Object

another variable that can hold multiple values

- we often use `const` data type for object

The values are written as `key**:value**` pairs (name and value separated by a colon)

```jsx
const students = { fullname: 'hanna kebede', age:29}
console.log(students['fullname'])
console.log(students.fullname')
/*
logs
hanna kebede
hanna kebede
*/
```

can hold values of datatypes including arrays

```jsx
console.log(students['fullname'])

const person = {
  fistName: 'hanna',
  lastName: 'kebede',
  age: 23,
  skills: [
    'HTML', 'CSS', 'React'
  ]
}
```

### Getting values from an object

1. using `.key_word`
    
    ```jsx
    console.log(person.firstName)
    ```
    
2. using `['key_word']`
    
    ```jsx
    
    console.log(person['firstName'])
    ```
    

### Creating object methods

function inside object

`this` used to access values of different properties of the object

```jsx
const person = {
  firstName: 'Asabeneh',
  lastName: 'Yetayeh',
  age: 250,
  country: 'Finland',
  city: 'Helsinki',
  skills: [
    'HTML',
    'CSS',
    'JavaScript',
    'React',
    'Node',
    'MongoDB',
    'Python',
    'D3.js'
  ],
  getFullName: function() {
    return `${this.firstName} ${this.lastName}`
  }
}

console.log(person.getFullName())
// Asabeneh Yetayeh
```

### Setting new key

```jsx
const person = {
  firstName: 'Asabeneh',
  lastName: 'Yetayeh',
  age: 250,
  country: 'Finland',
  city: 'Helsinki',
  skills: [
    'HTML',
    'CSS',
    'JavaScript',
    'React',
    'Node',
    'MongoDB',
    'Python',
    'D3.js'
  ],
  getFullName: function() {
    return `${this.firstName} ${this.lastName}`
  }
}
person.nationality = 'Ethiopian'
person.country = 'Finland'
person.title = 'teacher'
person.skills.push('Meteor')
person.skills.push('SasS')
person.isMarried = true

person.getPersonInfo = function() {
  let skillsWithoutLastSkill = this.skills
    .splice(0, this.skills.length - 1)
    .join(', ')
  let lastSkill = this.skills.splice(this.skills.length - 1)[0]

  let skills = `${skillsWithoutLastSkill}, and ${lastSkill}`
  let fullName = this.getFullName()
  let statement = `${fullName} is a ${this.title}.\nHe lives in ${this.country}.\nHe teaches ${skills}.`
  return statement
}
console.log(person)
console.log(person.getPersonInfo())
/*
Asabeneh Yetayeh is a teacher.
He lives in Finland.
He teaches HTML, CSS, JavaScript, React, Node, MongoDB, Python, D3.js, Meteor, and SasS.
*/
```

### Add new property

```jsx
let person = {
  name: "John",
  gender: "male"
};

person['age'] = 25;  // Using bracket notation

console.log(person);
//{ name: "John", gender: "male", age: 25 }
```

### Object methods

### `Object.assign({}, )`

To copy an object without modifying the original object.

```jsx
const copyPerson = Object.assign({}, person)
console.log(copyPerson)
```

### `Object.keys()`

To get the keys or properties of an object as an array

```jsx
const keys = Object.keys(copyPerson)
console.log(keys)
//['firstName', 'age', 'country','city', 'skills','title', 'address', 'getPersonInfo']
```

### `Object.values()`

o get values of an object as an array

```jsx
const values = Object.values(copyPerson)
console.log(values)
```

### `Object.entries()`

To get the keys and values in an array

```jsx
const entries = Object.entries(copyPerson)
console.log(entries)
```

### `hasOwnProperty()`

To check if a specific key or property exist in an object

```jsx
console.log(copyPerson.hasOwnProperty('name'))
console.log(copyPerson.hasOwnProperty('score'))
```

- to add to the array

`person.skills.push('SQL')`