## Loops in JAVA

Let's suppose you want to print numbers from 1 to 5 or let's say you want to print `Hello World!` 5 times on console. One approach to the problem can be as below,
```
System.out.println("Hello World!");
System.out.println("Hello World!");
System.out.println("Hello World!");
System.out.println("Hello World!");
System.out.println("Hello World!");
```
Now, what would you do if you have to print `Hello World!` a thousand times or a million times. Writing a million lines of code can be a solution but surely not an intelligent one. Not just the print statements, think of any set of instructions or tasks which you want to do repetitively. In cases like these, you can use loops. Loops are a utility to perform a task or set of tasks repetitively.

## Types of loops
There are three types of loops we'll be looking into
1. for loops
2. while loops
3. do-while loops

### For loops
_Syntax_
```
for (initialization; condition; increment/decrement) {
    body
}
```
Let's understand this by our previous example. Let's prin numbers from 1-5.
```
for(int num=1; num<=5; num++) {
    System.out.println(num);
}
```
- Initialization:

By writing `int num=1` we declare and initialize a variable `num` to value 1. Instead of declaring the variable inside the loop, we can also declare it before the loop and then just use it
```
int num;
for(num=1; num<=5; num++) {
    System.out.println(num);
}
```
- Condition

In the second part, we write a condition that our loop will check on every iteration. `num<=5` is the condition we wrote for our problem statement because we want to print the numbers from 1-5. There can be some different ways of writing conditions. The same condition `num<=5` can also be written as `num<6`. That makes sense right? Let the `num` be less than or equal to 5 or let it be less than 6 both are just different ways to accomplish the same result in the end.

You can also use a variable to specify conditions. For example, if you want to print numbers from 1-`n` where `n` is an integer entered by the user, you can do something like
```
Scanner input = new Scanner(System.in);

System.out.print("Please enter a number: ");
int n = input.nextInt();

for (int num=1;num<=n ;num++ ) {
    System.out.println(num);
}
```
output

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1637223010146/y_0pkQUXA7.png)

- Increment/decrement

Increment or decrement of the iteration variable (num) as per the need. In our case we want the variable to increase from 1 up to 5.

There are several ways you can increment/decrement the iteration variable.
- `num = num +1`: Increment by 1
- `num++`: Increment by 1
- `num+=1`: Increment by 1
- `num+=a`: Increment by `a`       (a is any integer)
- `num = num + a`: Increment by `a`

And same for decrement

When we run the loop, the variable `num` is initialized to `1`. Then the program checks for the condition, is `1<=5`? The answer is `true`. The body of the loop is executed and then the num is incremented by specified values (in our case incremented by 1), hence now `num=2`. Then the program again checks for the condition, is `2<=5`? The answer is `true` again so again the body is executed. This goes on until the 5 is printed and now the value of `num=6` because of increment. Now when the program checks for the condition, it'll get a `false` value so the program now gets out of the loop.

### While loops
_Syntax_
```
while (condition) {
    body
}
```
Let's try and implement our previous example, but this time with using while loop
```
int num = 1;
while (num<=5) {
    System.out.println(num);
    num++;
}
```
The working of a `while` loop is more or less the same as that of a `for` loop. We initialize a variable, we write a condition based on that variable, we write a body and then we increment the variable. The condition is checked at every iteration by the program.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1637223729464/dsY5jGVSq.png)

Now that we have understood both the loops, the question arises when to use the while loop and when to use the for loop.

You can use both of the loops interchangeably as you prefer. The reason that they both exist is
> Use the for loop when you know how many times the loop is gonna run

> Use the while loop if you do not know how many times the loop is gonna run.

For example, if you are given a problem to run the loop until the user inputs the letter `x`. It's not possible to achieve this using `for-loop` but you can do this using while loop as follows
```
Scanner input = new Scanner(System.in);
char ch = input.next().trim().charAt(0);
while (ch!='x') {
    System.out.println("Hello");
    ch = input.next().trim().charAt(0);
}
```
So now the loop will continue until the user inputs letter `x`.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1637224980989/1O5vKylzu.png)

_output_

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1637225064990/VkI7-jVGC.png)

### Do While loops
_Syntax_
```
do {
    body
} while (condition);
```
Loosely translated, a `do-while` loop can be read as
> do something (body), while the condition is true.

Implementing our previous example using the `do-while` loop
```
int num=1;
do {
    System.out.println(num);
} while (num<=5);
```
Again, one might ask himself, when do we use a `while` loop and when to use a `do-while` loop? What's the difference between the two of them?

If you observe, you might notice the difference between the two loops.
>In the case of while loops, the condition is checked first, and then the body is executed.

>In case of do-while loops body is executed and then the condition is checked.

From these, we can deduce that ___there might be the case where while loop will not run at all, but in all possibilities a do while loop will run at least once___.

Look at the following example
```
int num = 6;
while (num<=5) {
    System.out.println(num);
    num++;
} 
```
Here the iteration variable is already violating the condition, so the while loop will not run at all.
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1637226157328/1bNymD9hmD.png)

Now see what happens if we run a `do-while` loop in the same conditions

```
int num=6;
do {
    System.out.println(num);
} while (num<=5);
```

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1637226521759/AXtPQBR3d.png)

As we can see, though the condition is already violated, the loop still runs one time, it executes the body, and then after checking the condition it gets terminated.

So in cases where you want your loop to run at least once, you can choose `do-while` over `while` loop.

That's all about loops. Kunal has discussed some really important examples regarding Fibonacci numbers, Digit counts, Number reversal which is wholly based on the concepts that we have learned in this article. Do check out his video.

%[https://www.youtube.com/watch?v=ldYLYRNaucM]

Also, consider checking my repo for the code of those examples.

%[https://github.com/Raj-Pansuriya/java-dsa/]

Feel free to connect via socials

[Twitter](https://twitter.com/Raj_Pansuriya7)
[LinkedIn](https://www.linkedin.com/in/raj-pansuriya/)
[GitHub](https://github.com/Raj-Pansuriya/)
[Dev.to](https://https://dev.to/rajpansuriya)
