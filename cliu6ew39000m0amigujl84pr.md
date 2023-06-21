---
title: "Arrays"
seoTitle: "Arrays"
seoDescription: "Arrays in javascript"
datePublished: Tue Jun 13 2023 11:04:45 GMT+0000 (Coordinated Universal Time)
cuid: cliu6ew39000m0amigujl84pr
slug: arrays
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1686034342056/f9de5478-3947-4c89-b252-127393ad15ce.png
tags: javascript, arrays

---

# Introduction and Concepts

1. **Arrays:** Arrays are also known as lists and are data structures that organize items sequentially, one after another in memory.
    
2. **Sequential Organization:** Items in an array are stored in sequential order in memory. Each item is assigned an index, starting from zero and increasing by one for each subsequent item.
    
3. **Simplicity and Widely Used:** Arrays are considered the simplest and most widely used data structures. They are commonly used for storing and iterating over data.
    
4. **Contiguous Memory:** Arrays are stored in contiguous (adjacent) memory locations. This means that the elements in an array are stored next to each other in memory.
    
5. **Fast Lookup:** Accessing an element in an array by its index has a constant time complexity of O(1), which means it is very fast. The computer can directly retrieve the element using the index without iterating over the array.
    
6. **Array Size and Memory Usage**: The size of an array depends on the number of elements it contains. Each element occupies a specific amount of memory. For example, on a 32-bit system, if an array has four elements, and each element takes up four memory slots, the array would use 16 bytes of storage.
    
7. **Array Operations:**
    
    * **Push**: Adding an element to the end of an array (push operation) has a time complexity of O(1), as it simply appends the element to the existing array.
        
    * **Pop:** Removing the last element from an array (pop operation) also has a time complexity of O(1), as it directly accesses and removes the last element.
        
    * **On-shift**: Adding an element at the beginning of an array (on-shift operation) requires shifting all the existing elements to accommodate the new element. It has a time complexity of O(n) because it requires iterating and updating the indexes of all the elements.
        
    * **Splice:** Inserting an element in the middle of an array using the splice operation also requires shifting the subsequent elements. The time complexity for this operation is O(n) as well.
        

| Operation | Time Complexity | Methods in JavaScript |
| --- | --- | --- |
| lookup | O(1) | simply log the index |
| Push | O(1) | push |
| insert | O(n) | unshift, splice |
| delete | O(n) | splice |

1. **Pros and Cons:** Arrays are a good choice when you need to store and iterate over data, especially if you know the indices of the items. They have a small memory footprint and offer fast lookup and push operations. However, they may not be efficient for inserting or deleting elements, as it requires shifting the subsequent elements.
    

# Static & Dynamic Arrays

1. There are two types of arrays: static arrays and dynamic arrays.
    
2. Static arrays have a fixed size and require specifying the number of elements in advance.
    
3. Dynamic arrays automatically allocate memory and resize as needed.
    
4. Static arrays have the <mark>limitation of being fixed in size</mark> and <mark>may require copying the entire array</mark> to add more elements.
    
5. Dynamic arrays allow for <mark>adding elements without copying the entire array</mark> but may involve copying and moving existing elements in some cases.
    
6. <mark>Languages like JavaScript and Python use dynamic arrays by default,</mark> handling memory allocation automatically.
    
7. <mark>Dynamic arrays</mark> are generally more convenient as they <mark>eliminate the need for manual memory management.</mark>
    
8. <mark>Static arrays provide more control over memory </mark> but require manual resizing.
    
9. Understanding the underlying mechanisms of dynamic arrays can be beneficial.
    
10. Adding elements to a dynamic array may have a <mark>time complexity of O(n)</mark> in some cases, due to copying and moving existing elements.
    
11. Overall, dynamic arrays are more commonly used and preferred due to their automatic resizing capabilities.
    

### Static Arrays:-

| Operation | Time Complexity | Methods in JavaScript |
| --- | --- | --- |
| lookup | O(1) | simply log the index |
| **push** | O(1) | push |
| insert | O(n) | unshift, splice |
| delete | O(n) | splice |

### Dynamic Arrays:-

| Operation | Time Complexity | Methods in JavaScript |
| --- | --- | --- |
| lookup | O(1) | simply log the index |
| **append** | O(1) , {It can be O(n)} |  |
| insert | O(n) | unshift, splice |
| delete | O(n) | splice |

---

# Implementing Array from scratch in JavaScript

Array implementation is like deriving formulas - while solving problems, we're more focused on applying the formulas rather than actually deriving them. In interviews, you're unlikely to be asked to implement an array from scratch. However, knowing the derivation is like having an <mark>extra tool in your problem-solving toolbox.</mark> So, it's good to have that knowledge, just in case you encounter a sneaky question.

```javascript
// you will hardly be asked to implement array in an interview (its like derivation of formulas . While solving problems we are only concerned with applying the formulas and not actullly deriving the formula) But its good to konw the derivation

class myArray {
  constructor() {
    this.length = 0;
    this.data = {};
  }
  // get an element
  get(index) {
    return this.data[index];
  }

  push(item) {
    this.data[this.length] = item;
    this.length++;
    return this.length;
  }

  pop() {
    const lastItem = this.data[this.length - 1];
    delete this.lastItem;
    this.length--;
    return lastItem;
  }

  delete(index) {
    const itm = this.data[index];
    this.shiftItm(index);
  }

  shiftItm(index) {
    for (let i = index; i < this.length - 1; i++) {
      this.data[i] = this.data[i + 1];
    }
    this.data[this.length - 1]; // commment this and the last item wont be deleted
  }
}

const newArray = new myArray();
newArray.push("shahima");
newArray.push("you");
newArray.push("khushi");
newArray.push("Snaju");
console.log(newArray);
newArray.delete(1);
console.log(newArray);
```

```javascript
//OUTPUT                                                                      ─╯
myArray {
  length: 4,
  data: { '0': 'shahima', '1': 'you', '2': 'khushi', '3': 'Snaju' }
}
myArray {
  length: 4,
  data: { '0': 'shahima', '1': 'khushi', '2': 'Snaju', '3': 'Snaju' }
}
```

Here's an explanation of the code:

* The `myArray` class has a constructor that <mark>initializes the properties</mark> `length` and `data`. `length` represents the number of elements in the data structure, and `data` is an <mark>object that will store the elements.</mark>
    
* The `get(index)` method allows you to <mark>retrieve an element from the data structure by providing an index.</mark> It returns the element at the specified index in the `data` object.
    
* The `push(item)` <mark>method adds an item</mark> to the data structure. It assigns the item to [`this.data`](http://this.data)`[this.length]`, which means the <mark>item will be stored at an index equal to the current length of the data structure.</mark> The `length` is then incremented, and the new length is returned.
    
* The `pop()` the method <mark>removes the last item</mark> from the data structure. It retrieves the last item using [`this.data`](http://this.data)`[this.length - 1]`, decrements the `length`, and returns the last item. However, there is an issue in the code with the line `delete this.lastItem;`. It should be `delete` [`this.data`](http://this.data)`[this.length - 1];` to delete the last item from the `data` object.
    
* The `delete(index)` <mark>method removes an item from the data structure based on the provided index.</mark> It <mark>calls th</mark>e `shiftItm(index)` method to shift the remaining items in the `data` object to fill the gap left by the deleted item.
    
* The `shiftItm(index)` method is responsible for <mark>shifting the elements </mark> in the `data` object when an item is deleted. It starts from the provided index and iterates over the elements, <mark>moving each item one position to the left</mark>. However, there is an issue in the code with the line [`this.data`](http://this.data)`[this.length - 1];`. It should be `delete` [`this.data`](http://this.data)`[this.length - 1];` to remove the last item from the `data` object.
    

The code demonstrates the implementation of basic array-like operations using an object and associated methods. However, as noted in the provided comment, implementing an array is not a typical interview question. It's more important to understand and apply array operations rather than focusing on the internal implementation of an array-like structure.

> " In interviews, it's important to approach string-related questions as if they were array questions. When we think about it, strings are essentially arrays of characters. So, most of the time during an interview, when you encounter a question like "reverse a string," the best approach is to convert the string into an array.
> 
> You can achieve this by using a loop or utilizing string manipulation methods like `split()` in JavaScript. Once you have performed the necessary operations on the array, you can convert it back to a string before returning the final result.
> 
> Reversing a string is just one example of a common interview question where you manipulate strings. Remember to treat strings as arrays and apply array-related techniques. In the next video, we will demonstrate this concept further with a typical interview question. "

# Fundamental Problems

Remember Arrays are dynamic in Java Script.

## Reverse a string

Question:-

Write a function to reverse a string input:- "shahima", output:- "amihahs"

**Hints:-**

* **Instinctive Method:**\- Simply initialize another array and reverse it using for loop. (Not the best solution, bad space and time complexity)
    
* **In place (Temp variable) :** - Use a 3rd Variable to swap 1st and last elements and continue until the entire array is covered in half ( In place solution no new array creation )
    
* **Solution using Built-in Java Script methods**: - Use Split, reverse & Join. (Be aware the functions have their own time and space complexities)
    
* **ES6 One-line solution**:- Be aware the functions have their own time and space complexities
    
    ```javascript
    const dopemethod = (str) => console.log("5) " + [...str].reverse().join(""));
    ```
    

## Merge sorted Arrays

Question:

You are given 2 sorted arrays and their length as input (ex: a = \[1, 7, 9, 11\], m = 4, b=\[2, 6, 10\], n = 3). You have to merge them as one big array sorted array.

{You can give the answer as a different array, but the hint and solution for the **in-place** solution are also given}

* **Instinctive method**:- Initialize a separate array and compare both the given array using pointers and push the smaller one in the newly initialized array
    
* **In place (3-pointer method):-** Consider three-pointers
    
    int i = m - 1; int j = n - 1; int k = m + n - 1;
    

## Two sum

## Maximum subarray

## Move zeroes

## Contains Duplicate

## Rotate Array

# Resources

1. [Technical Interview Mind Map](https://coggle.it/diagram/W5E5tqYlrXvFJPsq/t/master-the-interview-click-here-for-course-link) (this map belongs to ZMT )
    
2. [Fundamental Interview Questions Github Repo](https://github.com/Shahimafiroz/dataStructures/tree/main/array)
    
3. [Try More On Leetcode](https://leetcode.com/problemset/all/?difficulty=EASY&page=1)
    
4. [My profile on leetcode](https://leetcode.com/khanshahima4/)
    
5. [Join() ----&gt; documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join) (converts array back to string)
    
6. [split() ------&gt; documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split) (converts a string to an array)
    
7. [reverse() ------&gt; documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reverse) (inbuilt reverse function in ES6)