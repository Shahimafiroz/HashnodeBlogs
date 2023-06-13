---
title: "Classes & Objects in Java Script"
seoTitle: "Classes and objects in java Script"
seoDescription: "This art demonstrates the concepts of instantiation, reference types, context, and scope in JavaScript. I"
datePublished: Mon Jun 12 2023 14:19:44 GMT+0000 (Coordinated Universal Time)
cuid: clisxxs7d000009mkcj3i597y
slug: classes-objects-in-java-script
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1686575669265/b54c452f-dc6c-497f-836c-d7f6d9b614e2.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1686579522624/b5d393f7-0597-4b53-ba1f-d2543ab06523.png
tags: constructor, objects, context, class-instantiation, refrence

---

In JavaScript, classes are a way to define blueprints for creating objects with similar properties and behaviors. They provide a syntax for creating objects based on a template or prototype. JavaScript classes were introduced in ECMAScript 2015 (ES6) and provide a more structured and familiar approach to object-oriented programming.

# Objects In JavaScript:-

Objects can be used to represent complex entities and enable the creation of more advanced data structures in JavaScript. They are a cornerstone of the language and are widely used in web development and other JavaScript applications.

Here are the key properties of objects in JavaScript:

1. **Key-Value Pairs:** Objects in JavaScript store data using key-value pairs, where <mark>each key is a string</mark> (or Symbol) and <mark>each value can be any data type.</mark>
    
2. **Object Literals:** Objects can be created using object literals, which are enclosed in curly braces `{}`. The key-value pairs are defined within the curly braces, <mark>separated by commas.</mark>
    
3. **Dot Notation:** You <mark>can access object properties using dot notation,</mark> where the object name is followed by a dot (`.`) and the property name.
    
    For example: `objectName.propertyName`.
    
4. **Bracket Notation:** Object properties can also be accessed using <mark>bracket notation, </mark> where the property name is enclosed in square brackets `[]`.
    
    For example: `objectName["propertyName"]`.
    
5. **Mutability:** Objects in JavaScript are mutable, meaning you can <mark>add, modify,</mark> or <mark>delete properties</mark> even after the <mark>object is created.</mark>
    
6. **Adding Properties:** You can <mark>add new properties to an object by assigning a value to a new key.</mark>
    
    For example: `objectName.newProperty = value`.
    
7. **Modifying Properties:** Existing properties can be modified by <mark>assigning a new value to the corresponding key.</mark>
    
    For example: `objectName.propertyName = newValue`.
    
8. **Deleting Properties:** You can remove properties from an object using the `delete` <mark>keyword</mark> followed by the object name and the property name.
    
    For example: `delete objectName.propertyName`.
    
9. **Object Methods:** Objects can have methods, which are <mark>functions stored as properties of the object</mark>. These methods can be accessed and invoked using dot notation.
    
    For example: `objectName.methodName()`.
    
10. **Object Constructors:** Objects can be created <mark>using constructor functions or classes, </mark> which provide a blueprint for <mark>creating multiple instances of objects</mark> with similar properties and behaviours.
    
11. **Object Prototype:** Objects in JavaScript inherit properties and methods from a prototype object, which allows for property sharing and method reuse.
    
12. **Object Serialization:** Objects can be <mark>converted to a string representation </mark> (serialization) using methods like `JSON.stringify()`, and can be parsed back into objects using `JSON.parse()`
    

# Object creation:-

In JavaScript, objects can be created and manipulated in different ways. <mark>Three concepts related to object creation and manipulation </mark> are reference types and instantiation.

## Reference Types:

In JavaScript, objects are reference types. This means that when you <mark>assign an object to a variable</mark> or pass it as a function argument, you're actually <mark>assigning a reference to the object rather than creating a new copy of it.</mark> This reference points to the object's location in memory.

For example:-

```javascript
let obj1 = { value: 10 };
let obj2 = obj1; // obj2 references the same object as obj1
obj2.value = 20;
console.log(obj1.value); // Output: 20
//also 
[]===[] // Output : false
```

## Context and Scope :

Context and scope are related concepts in JavaScript, as <mark>they both affect how variables and functions are accessed and behave within a program.</mark> While they are distinct concepts, they work together to determine the execution environment and the accessibility of variables and functions.

Here's how context and scope are related:

1. ***Scope Determines Variable Accessibility:*** Scope determines <mark>where variables and functions are defined and where they can be accessed</mark> within the code. Scopes are created by functions, blocks, and the global scope. <mark>The scope chain defines the hierarchy of scopes,</mark> allowing inner scopes to access variables and functions defined in outer scopes. So, the scope affects the visibility and availability of variables and functions within a specific context.
    
    * **Global Scope:** Variables and functions declared <mark>outside of any function or block have global scope.</mark> They are accessible throughout the entire JavaScript program.
        
    * **Function Scope:** Variables and functions declared <mark>inside a function are accessible only within that function </mark> and any nested functions.
        
    * **Block Scope:** Variables declared with `let` and `const` <mark>keywords inside a block (e.g., within an </mark> `if` <mark>statement or </mark> `for` <mark>loop) </mark> is limited to that block's scope and is not accessible outside of it.
        

***Context Determines the Value of "this":*** The value of the `this` keyword in JavaScript is determined by the context, which represents the <mark>object on which a function is being called</mark>. The context determines the execution context for a function and affects how it can access and interact with variables and functions.

* **Global Contex**t: In the global context (outside any function), `this` refers to the <mark>global object</mark> (e.g., `window` in a web browser or `global` in Node.js).
    
* **Function Context**: Within a function, `this` is <mark>determined dynamically at runtime,</mark> depending on how the function is called. It can refer to different objects based on the context of the function call.
    
* **Object Method Context:** When a <mark>function is called as a method of an object,</mark> `this` <mark>refers to the object itself</mark>. It allows the function to access and operate on the object's properties and methods.
    

**By combining scope and context, you can control the visibility and accessibility of variables and functions within different execution contexts**.

## Instantiation

Instantiation in JavaScript refers to the <mark>process of creating an instance or object based on a blueprint or template.</mark> It involves creating a new object that inherits properties and methods from a class or constructor function. There are several distinct fundamental ways to instantiate objects in Javascript:

1. ***Constructor Functions:***
    
    Constructor functions are traditional functions that are used with the `new` keyword to create objects. They define the structure and behaviour of the objects. Inside the constructor function, properties and methods are assigned to `this` keyword, which refers to the newly created instance.
    
    ```javascript
    function Player(name, age) {
      this.nameOfThePlayer = name;
      this.ageOfThePlayer = age;
      this.greet = function() {
        console.log(`Hello, my name is ${this.name} and I'm ${this.age} years old.`);
      }
    }
    
    const person = new Person('John', 25);
    person.greet(); // Output: Hello, my name is John and I'm 25 years old.
    ```
    
2. ***<mark>Classes (new keyword ):</mark>***
    
    ES6 introduced the class syntax, which provides a more convenient and intuitive way to define objects and their behaviour. Classes act as blueprints for creating objects, and instances are created using the `new` keyword. Classes have constructors that are used to initialize object properties.
    
    ```javascript
    class player {
      constructor(name, type) {
        this.playerName = name;
        this.playerType = type;
      }
    
      introduce() {
        console.log(`hi im ${this.playerName} , im a ${this.playerType}`);
      }
    }
    
    const wizard = new player("shahima", "High priestess");
    
    wizard.introduce(); // Output: hi im shahima , im a High prientess
    ```
    
    ***Object Literal Notation:***
    
    Object literal notation is a simple and concise way to create objects directly. It involves defining an object using curly braces `{}` and specifying the properties and methods within the object declaration.
    
    ```javascript
    const person = {
      name: 'John',
      age: 25,
      greet: function() {
        console.log(`Hello, my name is ${this.name} and I'm ${this.age} years old.`);
      }
    };
    
    person.greet(); // Output: Hello, my name is John and I'm 25 years old.
    ```
    
3. ***Factory Functions:*** Factory functions are functions that create and return objects. They encapsulate the object creation process and can customize the object's properties and behaviour before returning it.
    
4. **Object.create():**
    
    The `Object.create()` method allows you to create a new object with a specified prototype object. It creates a new object and sets the specified object as its prototype, allowing for prototypal inheritance.
    
    ```javascript
    const personPrototype = {
      greet: function() {
        console.log(`Hello, my name is ${this.name} and I'm ${this.age} years old.`);
      }
    };
    
    const person = Object.create(personPrototype);
    person.name = 'John';
    person.age = 25;
    person.greet(); // Output: Hello, my name is John and I'm 25 years old.
    ```
    

Each of these ways of instantiation has its own syntax and use cases. The choice of which method to use depends on the specific requirements of your code and your coding style preferences.

***<mark>We will discuss the use of constructors in Class along with inheritance (using ES6 Class Syntax ) for instantiation. This is the latest ES6 method of creating object instances for a class</mark>***

### Inheritance

Inheritance in JavaScript is a mechanism that allows objects to inherit properties and methods from other objects. It provides a way to create a hierarchy of objects where a child object can inherit the characteristics of its parent object.

There are multiple ways to implement inheritance in JavaScript, including:

1. Prototype Chain Inheritance
    
2. Constructor Inheritance
    
3. Object.create()
    
4. **<mark>ES6 Class Syntax:</mark>**
    
    The introduction of ES6 (ECMAScript 2015) introduced a class syntax to JavaScript that simplifies the implementation of inheritance. You can define classes using the `class` keyword, use the `extends` keyword to specify the parent class, and utilize the `super` keyword to call the parent's constructor and access its methods.
    
    ```javascript
    class ParentClass {
      constructor() {
        // parent class constructor
      }
    
      parentMethod() {
        // parent class method
      }
    }
    
    class ChildClass extends ParentClass {
      constructor() {
        super(); // calling parent class constructor
        // child class constructor
      }
    
      childMethod() {
        // child class method
      }
    }
    ```
    

### Using all of the above concepts

The code demonstrates the use of classes, inheritance, constructors, and method calls in JavaScript. It creates objects of different types (wizard and fighter) that inherit properties and methods from the `player` class, allowing for specific behaviors and functionality unique to each type of player.

```javascript
// INSTANTIATION

// involves a number of concepts 1. Constructors  2. inheritence 3.Principal class and derived Class

class player {
  constructor(nam, type) {
    console.log("player", this);
    this.playerName = nam;
    this.playerType = type;
  }

  introduce() {
    console.log(`hi im ${this.playerName} , im a ${this.playerType}`);
  }
}

// using inheritance

class wizard extends player {
  constructor(spell, powers, nam, type) {
    // console.log("wiz", this); never use the derived class before "super" it will give error
    super(nam, type);
    this.spellWiz = spell;
    this.powersWiz = powers;
    console.log("wiz", this);
  }

  castSpell() {
    console.log(
      `I ${this.playerName} posses the power of ${this.powersWiz} , and I now cast a spell ${this.spellWiz}`
    );
  }
}

class fighter extends player {
  constructor(killCapacity, killTime, nam, type) {
    super(nam, type);
    this.killfig = killCapacity;
    this.killtim = killTime;
  }

  fightBugs() {
    console.log(
      `I ${this.playerName} posses the kill capacity of ${this.killfig} , and I can kill for ${this.killtim}`
    );
  }
}

// now instantly creating new players(Objects) of different kinds(wizards and fighters) using main class(player) and derived class(fighters and wizards)

const wiz = new wizard(
  "Abra cadabra ",
  "Turning readers in coding wizards",
  "Shahima",
  " HighPriestess"
);
const Bugkiller = new fighter("1000", "0.1 seconds", "Khushi", "cyberQueen");

//
wiz.introduce();
wiz.castSpell();

Bugkiller.introduce();
Bugkiller.fightBugs();

// Out put

// player wizard {}
// wiz wizard {
//   playerName: 'Shahima',
//   playerType: ' HighPriestess',
//   spellWiz: 'Abra cadabra ',
//   powersWiz: 'Turning readers in coding wizards'
// }
// player fighter {}
// hi im Shahima , im a  HighPriestess
// I Shahima posses the power of Turning readers in coding wizards , and I now cast a spell Abra cadabra 
// hi im Khushi , im a cyberQueen
// I Khushi posses the kill capacity of 1000 , and I can kill for 0.1 seconds
```

***Explination:-***

1. Class Definitions:
    
    * The `player` class is defined with a constructor that takes `nam` and `type` parameters. It initializes the `playerName` and `playerType` properties.
        
    * The `player` class also has an `introduce` method that logs a message to the console, displaying the player's name and type.
        
    * The `wizard` class extends the `player` class using the `extends` keyword. It has a constructor that takes additional parameters `spell`, `powers`, `nam`, and `type`. It calls the parent class constructor using the `super` keyword and initializes the `spellWiz` and `powersWiz` properties.
        
    * The `wizard` class also has a `castSpell` method that logs a message to the console, displaying the player's name, powers, and the spell being cast.
        
    * The `fighter` class also extends the `player` class. It has a constructor that takes additional parameters `killCapacity`, `killTime`, `nam`, and `type`. It calls the parent class constructor using `super` and initializes the `killfig` and `killtim` properties.
        
    * The `fighter` class also has a `fightBugs` method that logs a message to the console, displaying the player's name, kill capacity, and kill time.
        
2. Instantiation:
    
    * Two instances are created: `wiz` of the `wizard` class and `Bugkiller` of the `fighter` class. They are initialized with specific values for the constructor parameters.
        
3. Method Calls:
    
    * The `introduce` and `castSpell` methods are called on the `wiz` object, logging the corresponding messages to the console.
        
    * The `introduce` and `fightBugs` methods are called on the `Bugkiller` object, logging the respective messages to the console.
        
4. Output:
    
    * The output shows the console logs from the constructors and method calls.
        
    * Initially, the constructors of the `wizard` and `fighter` classes log their respective objects, showing the initial values of the properties.
        
    * The `introduce` method of `wiz` displays the player's name and type.
        
    * The `castSpell` method of `wiz` displays the player's name, powers, and the spell being cast.
        
    * The `introduce` method of `Bugkiller` displays the player's name and type.
        
    * The `fightBugs` method of `Bugkiller` displays the player's name, kill capacity, and kill time.
        
    
    ## Entire example at glance
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1686653002064/17e803a5-4c23-4beb-a290-3ef236bc4f87.png align="center")