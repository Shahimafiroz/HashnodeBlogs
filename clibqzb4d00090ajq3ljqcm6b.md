---
title: "Unlocking the Mystery of Big O"
seoTitle: "Big O"
datePublished: Wed May 31 2023 13:32:53 GMT+0000 (Coordinated Universal Time)
cuid: clibqzb4d00090ajq3ljqcm6b
slug: unlocking-the-mystery-of-big-o
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1685773793135/0162752f-e941-4612-8ea1-59547fd179b1.png
tags: javascript, big-o-notation, javascriptdsa

---

# Factors determining good code

### Two major characteristics of a good code are:-

**Readability:**

Readable code is <mark>easy to understand and interpret by humans</mark>. It follows consistent coding styles, indentation, and formatting conventions. Meaningful variable and function names are used, making the code self-explanatory. Additionally, the code should be well-documented with comments, explaining the purpose of the code, algorithmic approaches, and any complex logic. Readable code enhances collaboration among developers, reduces bugs, and simplifies maintenance and debugging tasks.

**Scalability:**

Scalable code can handle growing demands and accommodate an increasing amount of data or users without significant performance degradation. It <mark>involves designing code</mark> that efficiently handles larger workloads by <mark>optimizing algorithms, data structures, and resource usage. </mark> Scalable code can be ***horizontally scalable*** *(adding more machines/nodes to handle the increased load)* or ***vertically scalable*** *(optimizing a single machine's capacity).* Scalable code is essential for applications that handle large-scale data processing or high-user traffic.

## A little bit more on scalability

When you talk about scalability as an engineer, there are two important factors to consider: speed and memory.

**<mark>Firstly, speed</mark>** refers to how quickly your code runs. You need to assess the runtime of your code and determine how much time it takes for a function to execute. It's essential to optimize your code to minimize the number of operations required and make it run as fast as possible.

**<mark>The second factor is memory.</mark>** Computers have limited memory resources, and you need to be mindful of how much memory your code consumes. Excessive memory usage can impact performance, even though computers nowadays have more memory compared to earlier times. It's important to consider the memory requirements of your code and ensure efficient utilization of resources.

As you write code, keep in mind ***<mark>these three pillars: readability, speed, and memory.</mark>*** Aim for clean and readable code that can be easily understood and maintained by others. Strive for efficient code with optimal time complexity to ensure good performance. Additionally, pay attention to memory usage and avoid unnecessary consumption to make the most of the available resources.

# Time Complexity

Time complexity refers to the measure of the amount of time or number of operations required by an algorithm to run as a function of the input size. It helps in understanding how the running time of an algorithm grows as the input size increases. Time complexity is usually expressed using Big O notation.

**For example,** if an algorithm has a time complexity of O(n), it means that the running time of the algorithm grows linearly with the size of the input. If the input size doubles, the running time of the algorithm also approximately doubles.

## Need for Big O

Your **timing will differ** from mine if you copy this code and run it on your PC. You're going to lose your cool since this code will fluctuate from run to run and not match my number. It **might go significantly faster or slower**. You see, a lot of other elements, including the computer's CPU power, the other programmes running on it, the programming languages you're using, and many others, all play a role in this. So, our runtime is affected by a variety of circumstances.

```javascript
// const slang = ['bruh'];
const slang = ["bruh" , "wtf" , "naur" , "lamo" , "lol" , "rolf" , "nvm" , "bimbo"];

function findingbruh(array){
  let t0 = performance.now();
  for (let i = 0 ; i < array.length ; i++ ){
    if (array[i] === "bruh"){
      console.log("bruh FOUND !!");
    } 
    // if
  } // for
  let t1 = performance.now();
  let res = t1 - t0 ;
  console.log("The time needed to search the slang " + res + " milliseconds" )
} // findingNemo

findingbruh(slang);
```

```javascript
bruh FOUND !!
The time needed to search the slang 3.996059998869896 milliseconds

```

**How can we ensure that there is a means to assess the efficiency of code,** identify excellent code, identify that code, and identify code that can scale such that when the number of inputs or arrays rises, it doesn't progressively get slower and slower? **<mark>When describing how long an algorithm takes to run, we utilise big notation.</mark>** We may compare it against various algorithms, or in this example, functions that use large O, and determine which one is better.

## What is Big O?

When we talk about Big O and the scalability of code, we are essentially referring to what happens as our input size grows larger and larger.

The key question is: How much does the algorithm or function slow down? Let's consider a list of characters, such as the characters in the movie "Finding Nemo," stored in an array. ***As we increase the number of characters in the array, we need to understand how many more operations or tasks we have to perform.*** This concept is known as algorithmic efficiency.

Big O notation allows us to precisely explain this concept. If we recall, in our function, we started with an array containing just one element, which was "Nemo." That one element represented the number of inputs in the function.

However, **as we gradually increase the size of the array** to include more characters, and even create a massive array with 100,000,000 elements, ***we notice that the number of operations or tasks we need to perform within the loop also increases significantly.*** <mark>It's important to note that different functions can have different complexities represented by Big O.</mark> This means that the number of operations can increase rapidly in some cases, while in others, it may not.

The O(1) algorithm, which stands for constant time complexity, is the best, as seen by the Big O graphic above. This suggests that your algorithm does not iterate and instead just processes one sentence. Then there are others like O(log n), which is nice, as seen below:

1. O(1) - Excellent/Best
    
2. O(log n) - Good
    
3. O(n) - Fair
    
4. O(n log n) - Bad
    
5. O(n^2), O(2^n) and O(n!) - Horrible/Worst
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685273328682/34ab8ee2-e839-440b-8c67-c9d194546a14.png align="center")

[Image credit](https://www.bigocheatsheet.com/)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685639987503/e0268d64-802e-4d75-8980-3e278bd3570d.png align="center")

[**Image credit**](https://www.geeksforgeeks.org/analysis-algorithms-big-o-analysis/)

**In summary,** Big O notation helps us analyze how the number of operations scales with the input size. It allows us to understand and compare the efficiency of different functions or algorithms, as well as how they handle larger inputs. By considering the number of operations rather than directly measuring time, we gain a clearer understanding of how the algorithm scales with larger inputs. This approach allows us to assess and compare the efficiency of different algorithms or functions based on the number of operations they require.

## O(n) {linear time}

**<mark>Linear time&nbsp;complexity is represented by O(n)</mark>** in Big O notation. It suggests that an algorithm's execution time increases linearly as the size of the input.

The **<mark>number of operations needed by an algorithm is directly proportional to the amount of the input when it has an O(n) complexity</mark>**. The method will carry out a fixed number of operations on each input element as the input size grows.

The algorithm will need n operations, for instance, if it iterates through an array of n elements and performs a certain action on each member. **<mark>The number of procedures will double as the input size does.</mark>**

The connection between the amount of input and the number of operations is described as being "linear" in this context. The time complexity of an O(n) algorithm would form a **<mark>straight line if it were plotted on a graph.</mark>**

It's important to note that O(n) complexity is <mark>typically seen as efficient</mark> because the execution time scales linearly with the input size. However, it's crucial to take into account additional elements, such as the activities' type and the precise specifications of the current issue.

*( Look at the chart for a relative comparison of O(n) with other complexities*)

Examples:

* for loop
    
* while loop
    
* do while loop
    
* for each loop
    

## O(1) {constant}

In Big O notation, **<mark>O(1) represents constant time complexity</mark>**. It indicates that the running time of an algorithm remains constant regardless of the input size.

When an algorithm has O(1) complexity, it **<mark>means that the number of operations required by the algorithm is fixed </mark>** and does not depend on the size of the input. Regardless of whether the input has 10 elements or 10,000 elements, the algorithm will perform the same number of operations.

This constant time complexity is often <mark>achieved when an algorithm directly accesses a specific element </mark> or performs a single operation, regardless of the input size. It does not require any loops or iterations that scale with the input.

**For example,** accessing an element in an array by its index or performing basic arithmetic operations like addition or multiplication are considered O(1) operations. These operations take a constant amount of time, irrespective of the size of the input.

The graph of O(1) complexity is a horizontal line parallel to the x-axis. It indicates that the time or number of operations required by the algorithm remains the same, regardless of the input size. This makes algorithms with O(1) complexity highly efficient, as they maintain consistent performance even with large inputs.

```javascript
const slang = ["dude", "wtf", "naur"]
function logTheSlangs(arra) {
  console.log(slang[0]);
  console.log(slang[1]);
}

logTheSlangs(slang);
```

```javascript
dude
wtf
```

But what will be the time complexity if there are 2 or more operations inside of the function?

In the given scenario, we are analyzing the number of operations performed by a function. Initially, we have three slang, and when we run the function, it performs two operations. So, regardless of the size of the boxes array, the function always runs two operations, resulting in O(2) complexity.

On a graph, this O(2) complexity appears as a flat line. <mark>We generalize this to O(1) or constant time</mark>, where the function takes a constant amount of time, irrespective of the input size. <mark>In terms of scalability, O(1) is excellent</mark> as it ensures consistent and predictable performance regardless of the input. It's like having a superhero power that handles any number of elements effortlessly.

### *Challenge*

**Challenge 1**:- Find the time complexity of the following function:-

```javascript
const input = shahima;
function challange (input) {

  let c  = 40 ; 
  c = 60 + 7 ; 
for (let i = 0 ; i < input.length ; i++ ){ 
    dumbfunc (); 
    let something = true ; 
    c ++ 
  }
  return c ;  
}
challange();
```

[**Answer**](https://replit.com/@shahimafiroz/findingNemo#challange1.js)

**Challenge 2:**\- Find the time complexity of the following function

```javascript
// What is the Big O of the below function? (Hint, you may want to go line by line)
function anotherFunChallenge(input) {
  let a = 5; 
  let b = 10;
  let c = 50;
  for (let i = 0; i < input; i++) {
    let x = i + 1;
    let y = i + 2;
    let z = i + 3;

  }
  for (let j = 0; j < input; j++) {
    let p = j * 2;
    let q = j * 2;
  }
  let who = "I don't know";
}
```

[Answer](https://replit.com/@shahimafiroz/findingNemo#challange2.js)

## Simplifying Big O

If you're concerned about having to calculate the time complexity step by step, as shown in the previous solutions, during interviews, let me assure you that it's not necessary. You won't be required to perform such detailed calculations.

During interviews, there are commonly followed guidelines that enable us to quickly determine the time complexity of a function without performing in-depth analysis.

By applying these rules, we can assess the function's complexity at a glance, without the need for detailed calculations. It saves time and allows us to promptly identify the type of time complexity associated with the function.

### Rules:-

1. **<mark>Worst Case</mark>**
    
    Analyze the function based on the input that would result in the maximum number of operations. This approach provides an upper bound on the time complexity.
    
2. **<mark>Remove constants</mark>**
    
    Drop the coefficients and constants when analyzing time complexity. For example, O(2n) is simplified to O(n), and O(3) becomes O(1).
    
3. **<mark>Different terms for inputs</mark>**
    
    Use different notations for different inputs.
    
    In the given example, the time complexity of the `printItems` function is
    
    <mark>O(n + m), </mark> where n represents the length of `array1` and m represents the length of `array2`.
    
    The time complexity is O(n + m) because the function iterates over each element of `array1` and `array2` separately using `forEach` loops. The time it takes to iterate over `array1` is proportional to the length of `array1` (n), and the time it takes to iterate over `array2` is proportional to the length of `array2` (m). Since the iterations are performed independently, the time complexities of the loops are added together.
    
    According to the rule of different terms for inputs, when analyzing the time complexity of a function with multiple inputs, each input is considered separately. In this case, `array1` and `array2` are different inputs. Therefore, the time complexity is expressed as O(n + m) rather than O(n \* m) because the loops iterate over the arrays independently rather than nested within each other.
    
    It's worth noting that the time complexity may vary if there are additional operations performed inside the loops that have their own time complexities. However, in the given example, where only console logging is performed, the dominant factor contributing to the time complexity is the iterations over the arrays.
    
    ```javascript
    const fruits = ["apple", "banana", "orange"];
    const colors = ["red", "yellow", "orange", "green", "blue"];
    
    function printItems(array1, array2) {
     array1.forEach(function(item) {
        console.log(item);
      });
     array2.forEach(function(item) {
         console.log(item);
         });
    
    }
    printItems(fruits , colors);
    ```
    
    ```javascript
    apple
    red
    yellow
    orange
    green
    blue
    banana
    red
    yellow
    orange
    green
    blue
    orange
    red
    yellow
    orange
    green
    blue
    ```
    
4. **<mark>Drop Non-Dominants</mark>**
    
    Identify the part of the function that grows the fastest as the input size increases. This dominant term usually determines the overall time complexity.
    
    For Example:-
    
    In the `numberAndSums` function, we have two loops: the first `forEach` loop and the nested `forEach` loop. The time complexity of the first loop is O(n), where n is the length of the `numbers` array. However, the nested loop, being a loop within a loop, has a time complexity of O(n^2).
    
    According to the dominant rule, when we have multiple factors contributing to the time complexity, we consider the one with the highest growth rate as the dominant factor. In this case, the nested loop has a higher growth rate compared to the first loop. As the input size (length of the `numbers` array) increases, the number of iterations in the nested loop grows quadratically.
    
    <mark>Hence the complexity is O(n^2) instead of O( n + n^2 )</mark>
    
    ```javascript
    const numbers = [1 , 2 , 3, 4 , 5, 6]
    
    function numberAndSums (numbers){
       
      console.log("these are the numbers");
       numbers.forEach(function(number){
         console.log(number);
       });
    
      console.log("These are the sum of each number with proceeding digit")
      numbers.forEach(function(firstNumber){
        numbers.forEach(function(secondNumber){
          console.log(firstNumber+secondNumber);
        })
        
      })  
    }
     numberAndSums(numbers);
    ```
    

***(Efficient tip 1:- Break the loops as soon as the conditions are met )***

## \*\*O(n^k) {\*\**The complexity of Nested loop*s}

When you see loops that are nested they have time complexity in the form of multiplication. The time complexity of nested loops is determined by the number of iterations performed by each loop. If you have 'k' nested loops, each iterating 'n' times, the overall time complexity would be O(n^k). This means that the time complexity grows exponentially with the number of nested loops. It is important to consider the impact of nested loops on the efficiency of your code, as excessive nesting can lead to slower execution times for large input sizes.

The two pairs problem:-

The time complexity of the `pairUpCombo` the function is O(n^2), where 'n' is the length of the `array`. This is because there are two nested loops, both iterating over the `array` with a length of 'n'.

The outer loop iterates 'n' times, and for each iteration of the outer loop, the inner loop also iterates 'n' times. As a result, the total number of iterations will be n \* n = n^2.

Therefore, the time complexity of this function is quadratic, indicating that the execution time will grow quadratically with the size of the input array. It is important to be mindful of such time complexities, especially for larger input sizes, as they can impact the performance of your code.

```javascript
//// all possible combinations
const colors = ["red", "yellow", "orange", "green", "blue"];

function pairUpCombo(array) {
  for (i = 0; i < array.length; i++) {
    for(j=0 ; j< array.length ; j++){ 
        console.log(array[i], array[j]) 
    }  
  }  
}
pairUpCombo(colors);
```

```javascript
red red
red yellow
red orange
red green
red blue
yellow red
yellow yellow
yellow orange
yellow green
yellow blue
orange red
orange yellow
orange orange
orange green
orange blue
green red
green yellow
green orange
green green
green blue
blue red
blue yellow
blue orange
blue green
blue blue
```

The time complexity of the `pairUpPerm` the function is O(n), where 'n' is the length of the `array`.

In this function, there is a single loop that iterates over the `array`. The loop runs from the first element of the array (`i = 0`) to the second-to-last element (`i < array.length - 1`). During each iteration, it prints the current element (`array[i]`) and the next element (`array[i + 1]`).

Since the loop iterates over each element of the array once, the time complexity is directly proportional to the size of the array, resulting in a linear time complexity of O(n).

The last line outside the loop (`console.log(array[array.length - 1], array[0])`) prints the last element of the array (`array[array.length - 1]`) and the first element (`array[0]`). This line executes in constant time and does not affect the overall time complexity of the function

```javascript
//permutations
const colors = ["red", "yellow", "orange", "green", "blue"];
function pairUpPerm(array) {
  for (i = 0; i < array.length - 1; i++) {
    console.log(array[i], array[i + 1]);
  }
  console.log(array[array.length - 1], array[0]);
}
pairUpPerm(colors);
```

```javascript
red yellow
yellow orange
orange green
green blue
blue red
```

## O(n!)

Ah, the dreaded beast of factorial time complexity! If you find yourself trapped in its clutches, something has gone terribly wrong. Brace yourself, for it's the costliest and steepest of them all. It's like a deep abyss where efficiency plummets. I won't even attempt a demonstration, as encountering it is as rare as spotting a unicorn. Nonetheless, let me introduce you to its mathematical notation, O(n!).

The notation O(n!) represents the time complexity of an algorithm or function, specifically indicating factorial time complexity. In computational complexity theory, it describes an algorithm whose running time grows factorially with the size of the input.

Factorial time complexity, denoted as O(n!), implies that the algorithm's execution time increases very rapidly as the input size (n) grows. For example, if the input size is 5, the algorithm would take 5! = 5 x 4 x 3 x 2 x 1 = 120 units of time to complete. As the input size increases, the execution time grows exponentially.

The factorial function represents the product of all positive integers less than or equal to a given number. For n! it is the product of all positive integers from 1 to n. This function is often encountered in combinatorial problems and can be associated with algorithms involving permutations, combinations, or exhaustive searches.

It's important to note that O(n!) represents an extremely inefficient time complexity. Algorithms with factorial complexity are generally considered impractical for large input sizes due to their exponential growth rate. It's advisable to explore more efficient algorithmic approaches or optimizations whenever possible to avoid using algorithms with factorial time complexity.

# Space Complexity

When you're running a program, there are two ways it remembers things: the heap and the stack.

The <mark>heap is where you typically store variables</mark> that you assign values to, while the <mark>stack is used to keep track of function calls.</mark>

Sometimes, you may want to optimize for using less memory instead of focusing on reducing the execution time. When we talk about memory or space complexity, it's similar to discussing the time cost. We look at the total size relative to the input size and consider how many new variables or memory we allocate and how much memory is being used.

Let's take an example to understand this better. Until now, we have mainly focused on time complexity and how fast and how many operations are required, but in real-life scenarios, memory is another important factor.

Imagine a <mark>box that represents the capacity of a function to handle input.</mark> If we have to create a large number of boxes to run this function efficiently, it may <mark>exceed the limited capacity and cause issues like a stack overflow</mark>. We will discuss this further when we cover recursion.

**So, what causes space complexity?**

1. Adding variables
    
2. Data structures (arrays, objects, and hash tables)
    
3. Function calls and
    
4. Allocations
    

contribute to space complexity.

# Recommended resources

Big O cheat Sheet:- [https://www.bigocheatsheet.com/](https://www.bigocheatsheet.com/)

More reference on Big O :- [https://www.geeksforgeeks.org/analysis-algorithms-big-o-analysis/](https://www.geeksforgeeks.org/analysis-algorithms-big-o-analysis/)