## Conditionals in JAVA

What makes programming so much more powerful are conditional statements. This is the ability to test a variable against a value and act in one way if the condition is met by the variable or another way if not. They are also commonly called by programmers _if statements_.

conditional statements, conditional expressions, and conditional constructs are features of a programming language, which perform different computations or actions depending on whether a programmer-specified boolean condition evaluates to true or false.

## Logical operators used to write conditions

Java supports the usual logical conditions from mathematics:

- Less than: `a < b`
- Less than or equal to: `a <= b`
- Greater than: `a > b`
- Greater than or equal to: `a >= b`
- Equal to `a == b`
- Not Equal to: `a != b`

These statements provide us either `true` or `false` value
Java has the following conditional statements:

## Different types of conditionals
- Use `if` to specify a block of code to be executed, if a specified condition is true

    ```
if (boolean expression true/false) {
    // block of code to be executed if the condition is true
}
code...
...
...
    ```
    If the condition is `true` then the code inside the code block is executed otherwise it is skipped and the program continues from the instruction after the `if-block`.

    For example, let say we want to decide on a bonus for various employees based on their salaries and then add the bonus to their salaries to get the final amount to be paid to that employee.

```
if (salary > 20000) {
    salary = salary + 2000
}
System.out.println(salary)

1) salary = 5000
output: 5000

2) salary = 20000
output: 20000

3) salary = 21000
output: 21000 + 2000 = 23000
```

- Use `else` to specify a block of code to be executed, if the same condition is false

    ```
if (boolean expression true/false) {
    // block of code to be executed if the condition is true
}
else {
    // block of code to be executed if the condition is false
}
code ...
.....
```
    If the condition is `true` then the code inside the `if-block` is executed otherwise the code inside `else-block` is executed.

    In our previous example, we might want to add a bonus of Rs.1000 for employees having salaries less than Rs.20000

```
if (salary > 20000) {
    salary = salary + 2000
}
else {
    salary = salary + 1000
}
System.out.println(salary)

1) salary=5000
output: 5000 + 1000 = 6000

2) salary=20000
output: 20000 + 1000 =  21000

3) salary=21000
output: 21000+2000=23000
```

Remember, only one of the two, either `if` or `else` blocks get executed. The two blocks are never executed simultaneously.

- Use `else if` to specify a new condition to test if the first condition is false
    ```
if (condition_1) {
    // block of code to be executed if the condition_1 is true
}
else if (condition_2) {
    // block of code to be executed if condition_1 is false and condition_2 is true
}
else if (condition_3) {
    // block of code to be executed if condition_2 is false and  condition_3 is true
}
else {
    // block of code to be executed if all the above conditions are false
}
code...
...
...
```
    You might have guessed the working of `if-else-if` statements. The program starts from the very first `if` statement, if the condition is true, the corresponding block is executed otherwise the program counter jumps onto the next `if` statement. At last, if none of the conditions is `true` then the last `else-block` is executed.

    In our previous example, we might want to add a bonus of Rs.5000 having a salary more than or equal to Rs.40000

```
if (salary >= 40000) {
    salary += 5000        // same as salary = salary + 5000
}
else if (salary > 20000) {
    salary += 2000        // same as salary = salary + 2000
}
else {
    salary += 1000        // same as salary = salary + 1000
}
System.out.println(salary)

1) salary = 45000
output: 45000 + 5000 = 50000

2) salary = 40000
output: 40000 + 5000 = 45000

3) salary = 21000
output: 21000 + 2000 = 23000

4) salary = 20000
output: 20000 + 1000 = 21000

5) salary = 10000
output: 10000 + 1000 = 11000
```
Just like the `if-else` code, in the `if-else-if` code only one of the code blocks is executed at a time. i.e., in the given example only one of the four (the three `if-block` and one `else-block`) code blocks will be executed.

### Nested if-else statements
Sometimes we may want to nest if statements so that we can check for more than one condition.

The syntax for a nested if...else is as follows −
```
if(Boolean_expression 1) {
   // Executes when the Boolean expression 1 is true
   if(Boolean_expression 2) {
      // Executes when the Boolean expression 2 is true
   }
}
```

In our previous example, we might want to add a bonus of Rs.3000 to the employees who have worked more than 5 years at our company. We can do that as follows
```
if (salary >= 40000) {
    salary += 5000        // same as salary = salary + 5000
    if (working_tenure > 5) {
        salary += 3000
    }
}
else if (salary > 20000) {
    salary += 2000        // same as salary = salary + 2000
    if (working_tenure > 5) {
        salary += 3000
    }
}
else {
    salary += 1000        // same as salary = salary + 1000
    if (working_tenure > 5) {
        salary += 3000
    }
}
System.out.println(salary)
```
Here we have added a nested if condition to all the previous if conditions that check the condition and add up the bonus of Rs.3000 if met true.

You can nest `else if...else` in a similar way as we have nested if statement.

#### Caution
Let's see some common mistakes which people tend to do while writing conditional statements.
1. Wrong order while specifying conditions in `if-else-if`
```
if (salary >= 20000) {
    salary += 2000        // same as salary = salary + 2000
}
else if (salary > 40000) {
    salary += 5000        // same as salary = salary + 5000
}
else {
    salary += 1000        // same as salary = salary + 1000
}
System.out.println(salary)
```
Look at the code above. The code seems perfectly fine at first. Now try running the code with a salary input of Rs. 50000. The output you will get will be `50000 + 2000 = 52000`. But this does not make any sense. 50000 is greater than 40000 so the final amount should have been 55000. What is it that gave us the wrong output?

    Remember when we discussed how `if-else-if` works, we said that 
    >The next condition is checked ONLY AND ONLY if the previous condition is wrong. 

    Rs.50000 is greater than 40000 but it is also greater than 20000. That means our first condition is `true` so the program won't even bother to check further conditions and will skip them. Hence we get the wrong output. The correct (Logically correct to be precise) code for our problem statement would be
```
if (salary >= 40000) {
    salary += 5000        // same as salary = salary + 5000
}
else if (salary > 20000) {
    salary += 2000        // same as salary = salary + 2000
}
else {
    salary += 1000        // same as salary = salary + 1000
}
System.out.println(salary)
```
    Understand that while writing `if-else-if` statements ___all our conditions have to be in DESCENDING/ASCENDING order___ so none of the conditions is skipped.

2. Ignoring the boundary cases while writing conditions
While writing conditions we should always consider boundary cases. Boundary cases are extreme values where our condition met `true` or `false`. 

    For example, in the code cell below,
```
if (salary > 20000) {
    salary += 5000        // same as salary = salary + 5000
}
else if (salary < 20000) {
    salary += 2000        // same as salary = salary + 2000
}
```
    boundary case is people having `salary = 20000`. While writing this code, we totally forgot to consider people with `salary = 20000`. So in the end, people having `salary > 20000` will get a bonus of Rs.5000; people having `salary < 20000` will get a bonus of Rs.2000 and people having `salary = 20000` will get no bonus which is a really stupid thing to do as a manager. So the logically correct code would be
```
if (salary >= 20000) {
    salary += 5000        // same as salary = salary + 5000
}
else if (salary < 20000) {
    salary += 2000        // same as salary = salary + 2000
}
```
Always try to avoid logical mistakes while writing conditionals.



That's all for this one. Hope you all have got the gist of conditionals and how to use them. Go through my repo and play with conditional programs.

%[https://github.com/Raj-Pansuriya/java-dsa/]

Feel free to connect via socials

[Twitter](https://twitter.com/Raj_Pansuriya7)
[LinkedIn](https://www.linkedin.com/in/raj-pansuriya/)
[GitHub](https://github.com/Raj-Pansuriya/)
[Dev.to](https://https://dev.to/rajpansuriya)