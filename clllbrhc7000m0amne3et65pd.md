---
title: "Brief Overview Of OOP"
datePublished: Mon Aug 21 2023 20:23:42 GMT+0000 (Coordinated Universal Time)
cuid: clllbrhc7000m0amne3et65pd
slug: brief-overview-of-oop
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1692529923494/2a43253d-5850-4988-8671-aa4e5952245c.png
tags: inheritance, abstraction, polymorphism, encapsulation

---

# Introduction

The four main core concepts in object-oriented programming are

* **Abstraction:** Simplify complex reality by focusing on essential attributes and behaviours while hiding unnecessary details.
    
* **Encapsulation:** Bundle data and methods that operate on that data within a single unit (class), controlling access and maintaining data integrity.
    
* **Inheritance:** Create new classes based on existing ones, inheriting their attributes and behaviours. This promotes code reuse and hierarchy formation.
    
* **Polymorphism:** Allow different classes to be treated as instances of a common superclass, enabling flexibility and extensibility in handling objects.
    
    *(This image doesn't belong to me)*
    
    ![Java: OOPS Concepts - Facing Issues On IT](https://i0.wp.com/facingissuesonit.com/wp-content/uploads/2019/09/oops-concept.jpg?resize=474%2C255&ssl=1 align="center")
    
    Before delving into their meanings let's break down the concept of an **object** first. An object is something from the real world, like a car, boat, or book, but it isn't always physical to touch. It can also be intangible, such as a dental appointment, a cinema seat reservation, or a bank account. In the world of object-oriented programming, an object is whatever matters in the software you're creating. It's anything you need to keep and manage data about. Another term for an object is an **entity**.
    

# Abstraction

Now, let's move on to the first fundamental idea in object-oriented programming: **abstraction**. Abstraction means simplifying reality. For instance, think of a person as an object. However, when designing an application to handle person-related data, you won't need to know everything about a person. Instead, you'd focus on the relevant data and tasks you want to perform.

*(This image doesn't belong to me)*

![AlgoDaily - Object Oriented Programming Class Principles - Abstraction](https://i.ibb.co/7Qg0MhB/abstraction.png align="left")

Abstraction allows you to define a general structure and behaviour for classes while leaving the specific details to their subclasses. It also promotes code reusability and separation of concerns. For example, you can create an abstract class-like **Shape** or an interface-like **drawable** to define common attributes and behaviours for different shapes in a graphics application. Concrete shapes like `Circle` and `Rectangle` can then extend the abstract class or implement the interface while providing their own specific implementations of the abstract methods.

1. To create objects in code, you require a **class**. A class acts as a template for constructing objects. It's code written by a programmer to define an object's attributes and operations.
    
2. Attributes describe the object and Sometimes, these are called **fields** because they hold data. Many programmers refer to them as **properties**. These properties are written in the class, either as public variables or as property procedures.
    
3. **Operations** are things that can be done with or to an object. They're sometimes seen as **behaviours**, but more commonly, they're known as **methods**. Methods are like programs within the class. They're coded as procedures or functions.
    
4. Think of a **class** as a template for making objects. It's like a pastry cutter: once it's made, you can use it to create lots of objects of the same kind. A class is sometimes called a **type**.
    
5. Each **object** is an example of a class in the computer's memory. Making an object from a class is called **instantiation**. Once these objects exist, you can give them values for their properties, making each object a unique thing.
    
6. The properties are defined in the class using property procedures. These procedures might have code to double-check property values when they're being set. This helps ensure the data inside the object is trustworthy. The values assigned to an object's properties are collectively referred to as the **state** of the object.
    

# Encapsulation

The **second core concept** in object-oriented programming is **encapsulation**. This involves concealing the intricate inner workings of an object from the software and programmers utilizing it. This is often referred to as **information hiding**, as it binds the data and manipulates functions within an object together, protecting them from external interference.

* In larger software development projects, seasoned programmers frequently develop the classes intended for use by junior programmers.
    
* These classes might be accessible as a **class library**. Some software development companies specialize in crafting new classes for use by other developers. Compiled class libraries safeguard their intellectual property.
    
    *(This image doesn't belong to me)*
    
    ![40+ OOPs Interview Questions and Answers (2023) - InterviewBit](https://s3.ap-south-1.amazonaws.com/myinterviewtrainer-domestic/public_assets/assets/000/000/062/original/encapsulation.png?1614861880 align="left")
    

To create an object from a class, set its properties, and invoke its methods, a programmer doesn't need to fully understand the class's internal mechanisms. The programmer only requires knowledge of the class's name, available properties and methods, and any required data when calling them. In essence, the programmer only interacts with the class's **interface**, while the underlying implementation code of those properties and methods can remain opaque. This simplifies object usage and ensures the encapsulated data and operations are secure.

## What is the difference between abstraction and encapsulation?

In essence, **abstraction** is about presenting a high-level overview of an object's capabilities without diving into specifics, while **encapsulation** is about bundling data and methods together to control access and protect the integrity of an object's internal state. These concepts work hand in hand to create well-organized and maintainable object-oriented programs.

| Aspect | Abstraction | Encapsulation |
| --- | --- | --- |
| **Focus** | Simplifying by highlighting essential features | Bundling data and methods together |
| **Purpose** | Manage complexity, provide a high-level view | Control access, and ensure data integrity |
| **Achieved by** | Abstract classes, interfaces | Access modifiers (public, private, etc.) |
| **What it Does** | Emphasizes what an object does | Focuses on how an object achieves tasks |
| **Example** | "Shape" class with "draw()" method | "getAge()" and "setAge()" methods |

Let's take an analogy to understand better

Imagine you're driving a car. The dashboard in front of you provides essential information like speed, fuel level, and engine temperature. Abstraction is like the car's dashboard, presenting essential information without revealing the complex mechanics. Encapsulation is like the car's engine compartment, bundling internal components and protecting them from external interference while offering controlled access.

# Inheritance

**Inheritance** is a core concept in object-oriented programming (OOP) where a new class (called a **subclass** or **derived class**) is created based on an existing class (called a **base class** or **superclass**). The subclass automatically inherits the attributes (data) and behaviours (methods) of the base class.

Inheritance allows you to:

* **Reuse Code:** You don't have to rewrite common code in every class. You define it once in the base class and reuse it in subclasses.
    
* **Extend Functionality:** Subclasses can add new methods and attributes or modify the inherited ones.
    
* **Create Hierarchies:** Subclasses can themselves become base classes, creating a hierarchy of related classes.
    

For example, if you have a base class "Animal" with properties like "name" and methods like "eat," you can create subclasses like "Dog" and "Cat" that inherit these properties and methods. Then, you can add specific methods like "bark" for the Dog class and "meow" for the Cat class.

*(This image doesn't belong to me)*

![Kotlin Inheritance with examples](https://beginnersbook.com/wp-content/uploads/2019/03/Kotlin_inheritance_example.png align="left")

In essence, inheritance allows you to build a structured and organized class hierarchy, making your code more efficient, maintainable, and adaptable.

Inheritance involves a few key concepts:

1. **Base Class (Superclass):** This is like the parent class, which holds common properties and methods. It's a blueprint for other classes to inherit from.
    
2. **Subclass:** Also known as a derived class, it's like a child class that inherits from the base class. It can add its own properties and methods or modify the inherited ones.
    
    ![Understanding Inheritance and Different Types of Inheritance](https://dotnettrickscloud.blob.core.windows.net/img/oops/types-of-inheritance-c-sharp.png align="left")
    
3. **Inherited Properties and Methods:** Subclasses automatically get all the properties and methods of the base class. It's as if they're passed down.
    
4. **Override:** Subclasses can modify or override methods inherited from the base class, allowing them to behave differently in the subclass.
    
5. **Extend:** Subclasses can add new properties and methods on top of what they've inherited from the base class.
    
6. **Hierarchy:** Inheritance creates a hierarchy of classes, where subclasses can themselves be base classes for other subclasses.
    
7. **Code Reusability:** Inheritance helps reuse code. Instead of writing the same code again for similar classes, you can define it once in the base class.
    
8. **IS-A Relationship:** Inheritance represents an "is-a" relationship. For example, a "Student" is-a "Person," or an "Employee" is-a "Person."
    

# Polymorphism

The **final core concept** in object-oriented programming is **polymorphism**. Polymorphism means that a class can redefine an inherited method in its own unique way. Consider a hierarchy where the base class is "Person" and has a method to save details of objects to a database. All classes in this hierarchy inherit this method and perform the same action.

However, sometimes, you might need to save details differently for specific objects. For instance, the "Customer" class could override the method to save its details to a different database. This is where polymorphism comes in. The "Customer" class can modify or replace inherited methods to create its version.

Polymorphism enables objects of the same type (like "Person" or "Customer") with the same interface to behave differently based on their specific implementations. This concept provides flexibility and customization in how objects handle common operations.

In simple terms, polymorphism allows different objects to have their unique ways of doing things while still adhering to a common interface. The word itself, "polymorphism," means "many forms," capturing the idea that objects of the same type can take on various behaviours.

## Types of polymorphism

Polymorphism in programming can be categorized into two main types: **Compile-time (or Static) Polymorphism** and **Runtime (or Dynamic) Polymorphism**.

1. **Compile-time Polymorphism (Static Polymorphism):**
    
    * Also known as **method overloading**.
        
    * Occurs when multiple methods with the same name but different parameters are defined within the same class.
        
    * The appropriate method to execute is determined at compile-time based on the method's parameters.
        
    * Example: Having methods like `calculateArea(int radius)` and `calculateArea(int length, int width)` in the same class.
        
2. **Runtime Polymorphism (Dynamic Polymorphism):**
    
    * Also known as **method overriding**.
        
    * Occurs when a subclass provides a specific implementation for a method that is already defined in its superclass.
        
    * The method to execute is determined at runtime based on the actual object's type.
        
    * Requires a **common interface** or **inheritance** between the superclass and subclass.
        
    * Example: Overriding a `displayInfo()` method in both the base class and a derived class, with each class providing its own implementation.
        

Both types of polymorphism contribute to the flexibility and versatility of object-oriented programming, allowing objects to behave differently based on their specific characteristics while maintaining a unified interface.

# Conclusion

In conclusion, Object-Oriented Programming (OOP) is a powerful paradigm that organizes code into objects, promoting code reusability, modularity, and easier problem-solving. The key concepts of abstraction, encapsulation, inheritance, and polymorphism provide a structured approach to building software systems that model real-world entities and interactions. OOP simplifies complex codebases, enhances maintainability, and enables efficient collaboration in software development.

**Here is a video that cohesively summarises all of the above concepts.**

[![](https://cdn.hashnode.com/res/hashnode/image/upload/v1692648306500/b92fce1f-eaf4-4e55-9a3e-8865a52b0c10.png align="left")](https://www.youtube.com/watch?v=m_MQYyJpIjg&list=PLWLsBsGulZlDSBpj96iL4tlpCQJDT43Iq&index=82)