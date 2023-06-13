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

# Implementing Array from scratch in JavaScript