---
title: "Java (variables And Data Types)"
datePublished: Mon Jun 13 2022 12:36:03 GMT+0000 (Coordinated Universal Time)
cuid: cl4cpyd3h06dljpnv70tt0m36
slug: java-variables-and-data-types
cover: https://cdn.hashnode.com/res/hashnode/image/unsplash/WkfDrhxDMC8/upload/v1655123645552/Ki-0Nnmjp8.jpeg
tags: java, community-classroom, shahimakhan

---

## DATA TYPES

Data types are various sizes and values that may be kept in a variable that is created for convenience and to cover all scenarios.

There are two types of data types
1. Primitive(p):- There are simply single values and no special abilities.
2. Non Primitive or reference(R):- contain a memory address of variable values 
(referenced data types start with capital letter in java)

the table below enlists the data types
![Screenshot 2022-06-13 at 4.47.04 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1655119047747/zY8AnNmlb.png align="left")

****IMP:- Data type declaration is required during compile time in static languages whereas dynamic languages can receive different data types over time.


## VARIABLES 

We assumed certain containers that housed numbers, much as we did in mathematics. Variables are used to store values in Java. We can store much more than numbers with these values, which are not restricted to numbers. We can store many different sorts of data values in a variable.

### 1. Creating and printing a variable


Creating a variable involves declaring the data type of the variable and the assigning the value to the the declared data type. Declaration and assigning when done simultaneously is known as initialization of a variable.


```

public class Main {
    public static void main(String[] args) {


        int a;      // declaration
        a = 10;    // assignment
        System.out.println(a);

        // using variables by 2nd approach

        long b = 39645478356474313L; // initialization

        System.out.println("The value of b var is: "+b);


    }

}

``` 

Output:-

![Screenshot 2022-06-13 at 5.08.23 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1655120351707/BUC7DFklP.png align="left")





Syntax for declaring all the data types as variables:-


```

public class Main {
    public static void main(String[] args) {

        int a = 456;
        float b =  3.345876f;
        double c = 1.102987634528;
        boolean d = true;
        long e = 273534244353636373L;
        byte f = 124; // note only between -127 to 127 ,hence not used much.
        short g = (short) 32768; // only between -32768 to 32768
        char symbol = '@';
        String name = "shahima";

        System.out.println("The value of a var is: " +a);
        System.out.println("The value of b var is: " +b);
        System.out.println("The value of c var is: " +c);
        System.out.println("The value of d var is: " +d);
        System.out.println("The value of e var is: " +e);
        System.out.println("The value of f var is: " +f);
        System.out.println("The value of g var is: " +g);
        System.out.println("The value of symbol var is: " +symbol);
        System.out.println("The value of name var is: " +name );



    }

}



``` 

Output:-


![Screenshot 2022-06-13 at 5.33.18 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1655121833980/SeL9VVnO1.png align="left")



### 2.Swapping 2 variables.

Assume you have a glass of lemon punch and a bowl of mango punch. If your mom asks you to put mango punch in the glass and lemon punch in the bowl. How would you do it ? You will need a temporary spare container to switch the contents. If you try to do it without a spare container you will end up mixing both the contents. That's what's happening in the code below.


```
public class Main {
    public static void main(String[] args) {

        int a = 456;
        int b =  334;
        int temp ;

        //before swapping
        System.out.println("\n before swapping\n");
        System.out.println("The value of a var is: " +a);
        System.out.println("The value of b var is: " +b);

        temp =a;
        a = b;
        b = temp;

        //After swapping
        System.out.println("\n after swapping\n");
        System.out.println("The value of a var is: " +a);
        System.out.println("The value of b var is: " +b);




    }

}



``` 

output:-
![Screenshot 2022-06-13 at 6.02.09 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1655123559536/X1CZvTOsA.png align="left")


 


