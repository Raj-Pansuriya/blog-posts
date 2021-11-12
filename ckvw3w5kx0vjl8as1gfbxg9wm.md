## Structure of JAVA Code

Till our last article, we have JDK installed in our system. Now we are all set to write our first Java code. You can make a separate directory (recommended) to contain all your java codes and projects
```
$ mkdir dsa_with_java
```
now to create a new java file
```
$ cd dsa_with_java
$ touch Hello.java
```
Have a look at the java code below. This is how a very basic java code looks like. It might feel overwhelming at first to know that we have to write so much just to have `Hello World!!` as output, but once we discuss all the building blocks of the code everything will start making sense
```
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello World!!");
    }
}
```
We will discuss everything that we have written in the code snippet shortly, but first, let's try and apply what we have already learned. Let's try and generate a byte code from the given code and try to have some output on our console.
As you can see, we only have a .java file currently in our folder. 

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1636699857397/niTJWf2nN.png)
Let's use the javac compiler to generate a .class byte code file.
```
$ javac Hello.java
```
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1636700116593/b5u8MUndl.png)
This is the file responsible for the platform independence of the Java language. That means, we can share this file with anyone irrespective of the Operating system he/she is using and they would be able to run the program just fine. Let's try and run the program now.
```
$ java Hello
```
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1636700409654/Ao-66tVGw.png)
Voila!!! We have successfully written and run our first java program.
Now let's understand all the things that we wrote in our code and their significance. You might not understand some of these keywords which is fine because it will start making sense once we learn object-oriented programming. So if you get everything now, it's well and good, but even if you do not get some things it's OK!!

## Some important things about a Java code
- Everything we write in java is going to be in _classes_
- Every file with a .java extension is a class itself
- The `Hello` class in `Hello.java` has to be public. You can not have a class named anything other than the file name. for example a file name Main.java has to have a public class named Main
- __public__: public means the class can be accessed from anywhere
- __class__: class keyword tells java to make a class. for example `class Hello` means make a class named `Hello`
- __main function__: Inside this public class we create a function named `main`. By convention, a java file must have a `main` function. It's the entry point for any java code. If there is no `main` function we won't be able to run that code. A function is nothing but a bunch of instructions.
- __public for function__: by writing public in line 2, we are making our main function public to all other modules. Think about it, We just said that the `main` function is the entry point of our program. So does it not make sense to make it public so even other classes can also access it. That is the reason we always have our main function declared public.
- __static__: Understand one thing, that if you have to use data or function of a class, you have to create an object of that class, and then only you can use those functions and data. Now `main` is the entry point of java. That means nothing exists in terms of code before executing the `main` function. But to use the main function we'll have to create an object of the `Hello` class. So we are stuck in a contradictory loop. To use a function we must have an object, but to create an object we should run the main function. So the thing is, we want to execute this `main` function without creating an object of `Hello` class. `static` is the keyword which provides us that power. `main` is the function that does not depend on objects and classes. Hence, it has to be a static function
- __void__: void is the return type of function. In java, every function has its return type.
for example, if we write a function to add two integers, its return type would be `int` because, in the end, the function will return us an integer (sum of two integers). In the same way, our main function here is just printing a simple message `Hello World!` and is not returning anything. Hence the return type void
- __String[] args__: These are known as command-line arguments. We can provide command-line arguments to our program and make our code execute in a particular way.
- We'll explore more about `System.out.println` in our coming articles. For now, consider it as a way to output some characters on the console.
## Tips while writing a java code.
- By convention, we write a class name in CapitalCase. It does not make any difference in the logic of the code even if you write it in a small case but it's a good practice to follow conventions of the language we are coding in.
- If you do not want your java code and byte code in the same folder you can do that by passing the `-d` flag to the java compiler. This is a good practice actually to keep all your source code (.java files) in the `src` folder and all the byte code in the `out` folder. It makes things well structured and organized.
```
$ javac -d location/to/save/byte/code file.java
```

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1636703313966/0YWMvtjIg.png)

That's all for this article. In the next article, we'll explore supported data types by Java. Till then feel free to connect with me on my socials.

[twitter](https://twitter.com/Raj_Pansuriya7)
[linkedin](https://www.linkedin.com/in/raj-pansuriya/)
[github](https://github.com/Raj-Pansuriya/)