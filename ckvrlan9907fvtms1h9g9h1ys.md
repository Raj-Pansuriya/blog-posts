## Introduction to Programming

## Programming
Programming in simple terms can be stated as a way of instructing computer to perform some task. We write a code and pass it to computer and the computer then performs tasks accordingly. The computer can only understand language of 0's and 1's, so we can say that programming at its heart is nothing but passing a stream of 0's and 1's computer.
Now, if internally its only 0's and 1's it would be very difficult for us to write all the instruction as a combination of 0's and 1's only. That is the reason we have different programming languages which allow us to write all those instructions in human redable format. Eventually computer is going to translate all that code into 0's and 1's but atleast we are saved from the the pain of writing all instructions in its naive form.

## Types of programming languages
1. Procedural language

  - These types of languages follow a top-bottom approach. That means, a series of well structured steps and procedures are specified to compose a program
  - It contains a systematic order of statements, functions and commands to complete a task
for example
```
Input 1st no.
input 2nd no.
add both numbers
print the answer
```

2. Functional languages

- In this programming approach, we write a code in pure functions only. A function in simple language is a block of code (set of instructions) bundled together.
- Used in situations where we have to perform the different operations on same type of data.

For example, let's say we have to print number of words containing in files and have 20 such files. Does it make sense to write the same code from scratch for each file. Instead what we can do is write a function to do the task and then just pass each file to that function (or in simple terms apply that function to each file).

Doing this not only saves time but is also helpful when we want to change the code due to some reason. Intead of having to chnage 20 differnet code files we can simply change the general function and we are good to go!

- These types of language follow ___first class function___ properties.
If we can reassign a function to another function then the language is said to follow first class function properties. for example,
```
function_1:
    some code block

instruction 1
instrcution 2

function_2=function_1
# here we assigned function_2 to be equal to function_1.
# This is known as 1st class function behaviour
```
An example of such programming language can be _python_. Mind that python may not follow purely functional language approach, I'm just saying that python does have first class functions.

3. Object Oriented Programming (OOP)

- Revolves around objects
- object = code + data

Let's say we have to gift 10 fruit baskets to our friends. We collected (40-Apples), (50-Oranges) and (70-Bsnanas) and divided them equally in those baskets. Now if someone asks us what fruit are we giving them, we do not have a single answer as the basket is composed of three different types of fruits. So then whats going to be the collective type of the basket. It'll be a custom type.

In the same way, when we are to group data of different datatypes like integer,decimal,character etc. the collective datatype of the data is custom datatype and one single unit of that data is said an object.

- So the idea of OOP is to divide the code into different chunks of code in order to develope, debug, reuse and maintain the software efficiently.

## Static vs Dynamic languages
Static | Dynamic
:-------:|:--------:
Type checking is done at compile time.`int a = 10`, we have to specify the type of `a` before assigning it a value. | Type checking is done at runtime.`a = 10`,  computer will automatically understand that `a` is of integer type as the values assigned is 10.
Errors will be shown at compile time.`int a = 25.4' will give an error after the compilation itself because we are assigning a decimal to an int type integer. &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; | Errors might not show till the program is run.`'a' + 10 //ERROR` all the statements before this particular statement will get executed (if none of them has any error ofcourse) and at the time of this statement itself we get an error because we are trying to add and integer and a character |
We have to declare datatype before using a variable `int a = 10` | No need to declare the datatype `a = 10` |
We may have to write a little more code as compared to dynamic language, but we have more control over the program. | Saves time in writing code but might give an error at runtime.

Now that we have got a basic background, let's try and understand some basic things which occur when we write some code.
 
## Memory Management

`a = 10`

In the given instruction, `a` is known as a ___reference-variable___ and the value `10` is known as an ___object___

There are two types of memories namely ___heap-memory___ and ___stack-memory___.

![Image description](https://cdn.hashnode.com/res/hashnode/image/upload/v1636431875362/L_xzUU0gC.png)

When the instruction `a = 10` is executed, the variable `a` is stored in stack-memory and it _points_ towards the object 10 which is stored in heap-memory.

![Image description](https://cdn.hashnode.com/res/hashnode/image/upload/v1636431877891/SWCZEomCI.png)
 

So whenever our code needs to access the value of `a`, it looks into stack by which it gets a pointer to a value of heap memory upon following which it gets actual value of the variable `a`.

#### Important
- More than one reference variables can point to same object

for example same person is called by different names by his family, friends teachers, etc.

![Image description](https://cdn.hashnode.com/res/hashnode/image/upload/v1636431881341/ZFyvcpuvz.png)

- Value of an object is changes for all the reference variables even if it is changed by any one reference variable

for example, if the person named Kunal has lunch, automatically baby, son and brother also had lunch.
- Objects with no reference variables are removed when garbage collection hits and the memory is freed.

for example,

`a = 10`
![Image description](https://cdn.hashnode.com/res/hashnode/image/upload/v1636431883533/WHtC0QdO6.png)
Now,we reassign a to 37

`a = 37`
 ![Image description](https://cdn.hashnode.com/res/hashnode/image/upload/v1636431885779/Vk1oDGnNt.png)

So the 10 will be removed from memory by garbage collector and the memory will be freed

Note:
- __Compile time__: The period where code from human redable format is being converted to machine redable format(machine code; 0's & 1's)
- __Run time__: The period where our code is being executed
- There are no separate partitions or disks as heap and stack, it is just how the memory is managed by CPU. There is only one RAM which is managed in the said way

#### Reference
{% youtube wn49bJOYAZM %}