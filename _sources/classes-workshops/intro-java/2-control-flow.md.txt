# 2 - Intro and Control flow

[Slideshow](https://docs.google.com/presentation/d/1guorgyU68cKTfepvvsMLYtrrQHuN8Rys6UL-r0_Ztsk/edit)

The recording will be published as soon as possible.

The class went over:
* Java basics (recap of [lesson 1](1-java-basics.md))
* Conditionals
* For and while loops

## Guide

%% TODO

## Demonstrated code
```{code-block} java
:caption: App.java
:lineno-start: 1

public class App {
    public static void main(String[] args) throws Exception {
        System.out.println("Hello, World!");
        String str1 = "first string";
        str1 = "second string";
        System.out.println(str1);

        int numOne = 4;
        int numTwo = 9;
        int numSum = numOne + numTwo;
        int numDiff = numOne - numTwo;
        int numProd = numOne * numTwo;
        int numQuot = numOne / numTwo;
        System.out.println(numSum);
        System.out.println(numDiff);
        System.out.println(numProd);
        System.out.println(numQuot);

        int a = 5;
        int b = 10;

        if (a==b){
            System.out.println("a = b");
        }
        else if (a<b){
            System.out.println("a < b");
        }
        else{
            System.out.println("a > b");
        }

        if (a < 10 && b > 5){
            System.out.println("a is less than 10 AND b is greater than 5");
        }
        else if (a < 10 || b < 5 || !(a==b))  {
            System.out.println("a is less than 10 OR b is less than 5");
        }
        else if (a!=b) {
            System.out.println("a is NOT equal to b");
        }
        else {
            System.out.println("neither of the conditions were true");
        }
        int j = 0;
        while (j<5){
            System.out.println("j is currently: " + j);
            j++;
        }

        for (int y = 0; y<=3; y++){
            System.out.println("Outer loop y = " + y);
            for (int z = 1; z <=2; z++){
                System.out.println("  Inner loop z = " + z);    
            }
        }
    }
}
```

## Exercise

* Write a program to check if the grade percentage in a variable is an A, B, C, or D. 
  * A = 90+, B = 80+, C = 70+, D = 0-69.9
    * Use a loop to go through numbers from 50 to 94, inclusive
    * In increments of 4

* Hint:
  * Think about what type of loop would be better
  * How you would increase something by 4 and use it?

### Solution

:::{dropdown} Solution
```{code-block} java
:caption: GradeChecker.java
:lineno-start: 1

public class GradeChecker {
    public static void main(String[] args) {
        // Loop from 50 to 94 in increments of 4
        for (int grade = 50; grade <= 94; grade += 4) {
            // Check grade category
            if (grade >= 90) {
                System.out.println("Grade " + grade + " = A");
            } else if (grade >= 80) {
                System.out.println("Grade " + grade + " = B");
            } else if (grade >= 70) {
                System.out.println("Grade " + grade + " = C");
            } else {
                System.out.println("Grade " + grade + " = D");
            }
        }
    }
}
```
:::
