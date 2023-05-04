Download Link: https://assignmentchef.com/product/solved-cse021-lab10-inheritence
<br>
We will use examples given in the lecture to extend the behavior of basic Counters. This lab is meant to familiarize you with the usefulness and concepts of class inheritance. It means traits and behaviors of the parent/super- classes will be passed down to the child/sub- classes.

<strong>Before you get started</strong>, read chapters 10.1, 10.2, 10.3 and 10.4. Answer the Assessment questions as you encounter them in the next section. The prompts for answering assessment questions are placed immediately following the material to which the listed questions relate.

<h1>Getting Started</h1>

After following the import instructions in the assignment page, you should have a Java project in Eclipse titled Lab 21_10. This PDF document is included in the project in the <strong>doc</strong> directory. The Java files you will use in this lab are in the <strong>src/oop</strong> directory.

<h2>Part 1: Test Counter.java using Runner.java</h2>

Counter class represents a counter that can be initialized and reset to 0, incremented by 1, and asked for its current value.

public class Counter {

private int myCount = 0;




public void increment() {

myCount++;

}




public int value() {   return myCount;

}




public void reset() {

myCount = 0;

}

}




It doesn’t have a main method; we’ll use the Runner class to run and manipulate it.




[Answer assessment questions 1 and 2]




Using the provided Runner class, along with calls to Counter methods, create a counter whose value is 3 (The code should go inside the testCounter method).




Create another counter that uses exactly seven calls to the reset and increment methods to end up with a value of 3 (The code should go inside testCounter7Statements method).

<h2>Part 2: Fill-in ModNCounter.java</h2>

“Mod N” counters count to a specified value (“N”), and then cycle back to zero. For example, when N = 3, the mod N counter will count as follows: 0, 1, 2, 0, 1, 2, 0, … .

The mod N counter has an extra instance variable — that we name cycleLength — and is initialized with a 1-paramter constructor whose argument is the intended N value. Thus, the following code




ModNCounter c = new ModNCounter(2);  System.out.println(c.value());   c.increment();

System.out.println(c.value());  c.increment();

System.out.println(c.value());  c.increment();




should print 0, then 1, and then 0.




Your task is to fill in ModNCounter so it has the behavior described here. You should only override the increment method and making no other changes to produce the desired behavior.




[Answer assessment questions 3, 4, 5 and 6]

<h2>Part 3: Create ModNCounter2.java</h2>

Create this class so it inherits from Counter. Objects of this class will behave exactly the same as counters of type ModNCounter, but with a different cycleLength. For the ModNCounter2 class, you should create an instance variable, a 1-parameter constructor, this time only override the value method, and make no other changes to produce the desired behavior. For the class that is creating and using ModNCounter2, it should appear to behave exactly the same as ModNCounter, but with a different modulus (“N” value). Be sure to include the line “package oop” at the top of this file.




[Answer assessment question 7]




Implement a method called testModNCounter2 to test ModNCounter2 in Runner (and call the method from main) so you know it is working. Be sure this new code is included in what you submit for Runner.java.

<h2>Part 4: Create DecrementableCounter.java</h2>

One might wish for a counter that allows decrementing its value as well as incrementing it. Create a class DecrementableCounter that inherits from Counter and provides a decrement method. If the counter’s value is 0, a call to decrement should have no effect. Otherwise, it should reduce the counter’s value by 1. Don’t change the Counter class to implement decrement. Once again, be sure to include the line “package oop” at the top of this file.




[Answer assessment questions 8 and 9]




Implement a method called testDecrementableCounter to test DecrementableCounter in Runner (and call the method from main) so you know it is working. Be sure this new code is included in what you submit for Runner.java.

<h2>Part 5: Fill-in SeasonCounter.java</h2>

Complete the SeasonCounter class that cycles through the four seasons. It will inherit from ModNCounter, overriding the toString method to return “spring”, “summer”, “fall”, or “winter”, depending on whether the current value is 0, 1, 2, or 3.




[Answer assessment question 10]




Implement a method called testSeasonCounter to test SeasonCounter in Runner (and call the method from main) so you know it is working. Be sure this new code is included in what you submit for Runner.java.

<strong> </strong>

<h1>Part 6: (Assessment) Logic Check and Level of Understanding</h1>

Create a Word document or text file named Part6 that contains answers to the following:

<ul>

 <li>The Counter class doesn’t have a constructor. Why doesn’t it need one?</li>

 <li>The Counter class doesn’t have a main. Why doesn’t it need one?</li>

 <li>How do we know ModNCounter inherits from Counter (what is the keyword)?</li>

 <li>Which method is the constructor inside ModNCounter class?</li>

 <li>Is cycleLength variable visible to the parent Counter class?</li>

 <li>What happens when we call value and reset methods for ModNCounter since it is not defined in ModNCounter?</li>

 <li>What happens when we call increment and reset methods for ModNCounter2 since it is not defined in ModNCounter2?</li>

 <li>Does decrement exist inside Counter?</li>

 <li>Does increment’s behavior change for DecrementableCounter? 10) Where is toString being inherited from?</li>

</ul>