---
title: "Strings & String Builder in JAVA"
datePublished: Thu Aug 31 2023 16:45:45 GMT+0000 (Coordinated Universal Time)
cuid: cllzedpli000b09k5fet3hmqu
slug: strings-string-builder-in-java
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1693499150453/7e9b9746-2106-4ab8-89b5-84d589001369.png

---

In Java, both `String` and `StringBuilder` are classes used to work with sequences of characters. However, they serve different purposes and have distinct characteristics.

# **String:**

* `String` is a class that represents an immutable sequence of characters. Immutable means that once a `String` object is created, its contents cannot be changed. If you want to modify `String`, a new `String` object is created with the modified content.
    
* Since `String` objects are immutable, and operations like concatenation, substring extraction, and manipulation result in the creation of new `String` objects. This can lead to performance issues when dealing with a large number of modifications, as memory allocation and copying take place.
    
* Example:
    
    ```java
    String str = "Hello";
    str = str + " World"; // Creates a new String object
    ```
    

Certainly! Here are some essential concepts and methods related to working with strings in Java:

### **1 String Creation and Initialization:**

* Creating a string literal: `String str = "Hello";`
    
* Creating a string using the `new` keyword: `String str = new String("Hello");`
    

### **2\. String Concatenation:**

* Using the `+` operator: `String result = str1 + str2;`
    
* Using the `concat()` method: `String result = str1.concat(str2);`
    

### **3\. String Length:**

* Getting the length of a string: `int length = str.length();`
    

### **4\. Accessing Characters:**

* Getting a character at a specific index: `char c = str.charAt(index);`
    

### **5\. Substring Extraction:**

* Getting a substring: `String substr = str.substring(startIndex, endIndex);`
    

### **6\. String Comparison:**

* Comparing strings for equality: `boolean isEqual = str1.equals(str2);`
    
* Comparing strings (case-insensitive): `boolean isEqualIgnoreCase = str1.equalsIgnoreCase(str2);`
    
* Checking if a string starts with/ends with a specific substring: `boolean startsWith = str.startsWith("Hello");` / `boolean endsWith = str.endsWith("World");`
    

### **7\. Searching and Indexing:**

* Finding the index of a specific character or substring: `int index = str.indexOf("lo");`
    
* Finding the last index of a specific character or substring: `int lastIndex = str.lastIndexOf("l");`
    

### **8\. String Manipulation:**

* Converting to uppercase/lowercase: `String upper = str.toUpperCase();` / `String lower = str.toLowerCase();`
    
* Removing leading and trailing whitespace: `String trimmed = str.trim();`
    
* Replacing characters/substrings: `String replaced = str.replace("l", "L");`
    

### **9\. Converting to Other Types:**

* Converting a string to an integer: `int number = Integer.parseInt(str);`
    
* Converting a string to a double: `double value = Double.parseDouble(str);`
    

### **10\. StringBuilder Usage:**

* Creating a `StringBuilder`: `StringBuilder stringBuilder = new StringBuilder();`
    
* Appending to a `StringBuilder`: `stringBuilder.append("Hello");`
    
* Inserting into a `StringBuilder`: `stringBuilder.insert(index, " World");`
    
* Converting `StringBuilder` to `String`: `String finalString = stringBuilder.toString();`
    

These are some of the fundamental concepts and methods related to working with strings in Java. Understanding and effectively using these methods will enable you to manipulate and process strings in various ways.

# Unfortunately, the string wasn't enough!

(Coming soon!!)