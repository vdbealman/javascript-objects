# Objects, Properties, and Methods

In real life, a car is an **object**.

A car has **properties**; weight and color, and **methods** like start and stop.

![image](https://user-images.githubusercontent.com/65863183/166125513-ece27570-7770-491c-ac80-1ed2367c1623.png)


All cars have the same **properties**, but the property **values** vary from car to car.

All cars have the same **methods**, but the methods are **performed at different times**.

## JavaScript Objects

You learned JavaScript variables are containers for data values.

  - This code assigns a simple **value** (Fiat) to a **variable** named car:

```
let car = "Fiat";

```

Objects are variables too. However, objects may contain many values.

  - This code assigns **many values** (Fiat, 500, white) to a **variable** named car:

```
const car = {type:"Fiat", model:"500", color:"white"};

```
The values are written as **name:value** pairs (name and value separated by a colon).

> It is a common practice to declare objects with the ```const``` keyword.

## Object Definition

Define (and create) a JavaScript object with an object literal:
```
const person = {firstName:"Vicki", lastName:"Bealman", age:61, eyeColor:"hazel"};

```
Spaces and line breaks are not important. 
  - An object definition can span multiple lines:

```
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 50,
  eyeColor: "blue"
};
```

## Object Properties

The **name:values** pairs in JavaScript objects are called **properties**:

Property | Property Value | 
--- | --- |
firstName | Vicki | 
lastName | Bealman
age | 	61
eyeColor |	hazel

## Accessing Object Properties

Access object properties in two ways:

```
objectName.propertyName

```
or
```
objectName["propertyName"]

```
> Example 1

```
person.lastName;

```

> Example 2

```
person["lastName"];

```

> JavaScript objects are containers for **named values** called properties.

## Object Methods

Objects can also have **methods**.
  - Methods are actions which can be performed on objects.
  - Methods are stored in properties as **function definitions**.

Property | Property Value | 
--- | --- |
firstName | Vicki | 
lastName | Bealman
age | 	61
eyeColor |	hazel
fullName | ```function() {return this.firstName + " " + this.lastName;}```

> A method is a function stored as a property.

**Example**

```
const person = {
  firstName: "John",
  lastName : "Doe",
  id       : 5566,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};
```
In the example above, ```this``` refers to the **person object**.
  - ```this.firstName``` means the ``firstName`` property of ```this```.
  - ```this.firstName``` means the ```firstName``` property of ```person```.

## What is ```this```?

In JavaScript, the ```this``` keyword refers to an **object**.
  - **Which** object depends on how ```this``` is being invoked (used or called).
  - The ```this``` keyword refers to different objects depending on how it is used:

  - In an object method, ```this``` refers to the **object**.
  - Alone, ```this``` refers to the **global object**.
  - In a function, ```this``` refers to the **global object**.
  - In a function, in strict mode, ```this``` is ```undefined```.
  - In an event, ```this``` refers to the **element*** which received the event.
  - Methods like ```call()```, ```apply()```, and ```bind()``` can refer ```this``` to **any object**.

> ### Note
> ```this``` is not a variable. It is a > keyword. You cannot change the value of ```this```.

## The ```this``` Keyword

In a function definition, ```this``` refers to the "owner" of the function.

In the example above, ```this``` is the **person object** which "owns" the ```fullName``` function.
  - ```this.firstName``` means the ```firstName``` property of **this object**.

## Accessing Object Methods

You access an object method with the following syntax:

```
objectName.methodName()

```
**Example**
```
name = person.fullName();

```
If you access a method **without** the ```()``` parentheses, it will return the **function definition**:

**Example**

```
name = person.fullName;

```
## Do Not Declare Strings, Numbers, and Booleans as Objects!

When a JavaScript variable is declared with the keyword "```new```", the variable is created as an object:

```
x = new String();        // Declares x as a String object
y = new Number();        // Declares y as a Number object
z = new Boolean();       // Declares z as a Boolean object
```

Avoid ```String```, ```Number```, and ```Boolean``` objects. 
  - They complicate code and slow down execution speed.






