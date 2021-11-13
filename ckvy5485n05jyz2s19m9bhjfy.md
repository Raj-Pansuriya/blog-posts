## I/O in JAVA

In our last article we discussed everything but output statement in our sample code. Let us explore inputs, outputs, classes responsible for I/O and packages in Java.

## What is a package in Java
In simple terms package is nothing but a folder in which our Java file will lie. Sometimes we may want to have a set of rules for our code files like
- A function should be accessed by files in that folder only.
- A class and its methods should be accessed by a aprticular folder files only
- A file should be accessed by files in `app` folder.
Its scenarios like this when we can make use of packages and access modifires. If you do not know what an access modifire, no worries because we will discussing that in detail later on. We have even used an access modifire named `public` which I explained in last article.

You might stumble upon packages now and then in your java code. Specially if you use an IDE, beacuse IDE's are set to create package for our program by default. Even if you do not use any IDE, you might use packages efficieantly to have some security for your code.

## Outputs in Java
We know that everything in Java works in classes. Java language provides us with some basic functionalities such as input, output, debugging, etc. which we can use while writing our program. 

One of such functionality is when we have to print something on our console. We use `print` or `println` function to print somethig on out console.

Now Java has a class called `System` in `java.lang` package (language package). You can actually open the file and inspect System class if your Development environment (IDE or Text editor) supports it. You can try click on `System` while holding `ctrl` key to open System class.
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1636819197687/LDb5WE38c.png)

The `System` class has a variable of type `PrintStream` named `out` that is used to print some output when given a stream of characters. The `out` variable has various functions for giving various types of output. One of them is `println` function which prints character output when given character input. In a nutshell, by writing `System.out.println()` we are accessing the println function to have the required output. Memorize it for now if any of above do not make sense to you.  It will make more sense when you know a bit more about classes.

#### print vs println
Both the function give us a standard output on teh console with a minor difference that println adds new line to the out put. Take a look at example below
```
public class Hello {
    public static void main(String[] args) {
        System.out.print("Hello World!!");
        System.out.print("My name is Raj!");
    }
}

output:
Hello World!!My name is Raj!
```
```
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello World!!");
        System.out.println("My name is Raj!");
    }
}

output:
Hello World!!
My name is Raj!

```
As you can see, a newline gets added at the end when we use prinln.

## Inputs in Java
As we have `System` class for handling outputs, in the same way we have a class to handle inputs in Java known as `Scanner` class. Its available in the `java.util` package. In order to use that class first we have to import `java.util` package in our program.
```
import java.util.Scanner;
```
Now how do we use a class, we create an object of it. `new` is the keyword used to make objects of a class. Now Scanner class has to be given an argument stating the source from where input is coming. The input may be from a file, it may be from a database, etc. In our case input is from keyboard, so we will pass `System.in`
Syntax for this is:
```
import java.util.Scanner;
public class Hello {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
    }
}
```
Now using object `input` we can take inputs from our user.
