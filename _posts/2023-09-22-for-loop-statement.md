---
author_profile: false
permalink: /java/for-loop-statement/
title: "For Loop"
last_modified_at: 2023-09-22T12:42:38-04:00
toc: true
toc_sticky: true
sidebar:
   title: "Java Notes"
   nav: java-notes
mermaid: true     

---

{% include video id="utTDUygzjeY" provider="youtube" %}

# For loop
## Syntax
```java
    for(initialization; expr; inc/dec expr){
       //body 
    }
```
The 3 parts of the for loop are initialization, expression and increment/decrement, they should
be separated by semicolon ``;``

## Flowchart

<div class="mermaid">
flowchart TD
    A[Initialize the loop] --> B{check expression}
    B --> |True| C[Execute for block]
    B --> |False| D(Loop terminate)
    C --> E[increment / decrement]
    E --> B
</div>

``for`` loop is initialized first and then the boolean expression is checked. If the expression
evaluates to true, then the for block is executed, otherwise the loop terminates. If the ``for``
block is executed, then the increment or decrement updated to continue the loop

## Examples
```java
public class Demo28{
    public static void main(String[] args) {
        for (int i=1;i<=5;i++){
            System.out.println(i);
        }
    }
}
```
```
Output:
1
2
3
4
5
```

```java
public class Demo29{
    public static void main(String[] args) {
        for(int i=10; i > 5; i--){
            System.out.println(i);
        }
    }
}
```
```
Output:
10
9
8
7
6
```
```java
public class Demo30{
    public static void main(String[] args) {
        int i =1,j;
        for (j = 1; i <=5; ) {
            System.out.println("i= " + i);
            System.out.println("j= " + j);
            i++;
        }
    }
}
```
```
Output:
i= 1
j= 1
i= 2
j= 1
i= 3
j= 1
i= 4
j= 1
i= 5
j= 1
```
