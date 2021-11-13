## I/O in JAVA

In our last article, we discussed everything but the output statement in our sample code. Let us explore inputs, outputs, classes responsible for I/O and packages in Java.

## What is a package in Java
In simple terms, a package is nothing but a folder in which our Java file will lie. Sometimes we may want to have a set of rules for our code files like
- A function should be accessed by files in that folder only
- A class and its methods should be accessed by particular folder files only
- A file should be accessed by files in the `app` folder.
It's scenarios like this when we can make use of packages and access modifiers. If you do not know what an access modifier is, no worries because we will be discussing that in detail later on. We have even used an access modifier named `public` which I explained in the last article.

You might stumble upon packages now and then in your java code. Especially if you use an IDE because IDE's are set to create a package for our program by default. Even if you do not use any IDE, you might use packages efficiently to have some security for your code.

## Outputs in Java
We know that everything in Java works in classes. Java language provides us with some basic functionalities such as input, output, debugging, etc. which we can use while writing our program. 

One such functionality is when we have to print something on our console. We use `print` or `println` function to print something on our console.

Now Java has a class called `System` in `java.lang` package (language package). You can open the file and inspect the System class if your Development environment (IDE or Text editor) supports it. You can try clicking on `System` while holding the `ctrl` key to open System class.
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1636819197687/LDb5WE38c.png)

The `System` class has a variable of type `PrintStream` named `out` that is used to print some output when given a stream of characters. The `out` variable has various functions for giving various types of output. One of them is the `println` function which prints character output when given character input. In a nutshell, by writing `System.out.println()` we are accessing the `println` function to have the required output. Memorize it for now if any of the above does not make sense to you.  It will make more sense when you know a bit more about classes.

#### print vs println
Both the function give us a standard output on the console with a minor difference that `println` adds a new line to the output. Take a look at the example below
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
As you can see, a new line gets added at the end when we use `println`.

## Inputs in Java
As we have a `System` class for handling outputs, in the same way we have a class to handle inputs in Java known as the `Scanner` class. It's available in the `java.util` package. To use that class first we have to import `java.util` package in our program.
```
import java.util.Scanner;
```
Now how do we use a class, we create an object of it. `new` is the keyword used to make objects of a class. Now Scanner class has to be given an argument stating the source from where input is coming. The input may be from a file, it may be from a database, etc. In our case input is from the keyboard, so we will pass `System.in`
The syntax for this is:
```
import java.util.Scanner;
public class Hello {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
    }
}
```
Now using object `input` we can take inputs from our user.
```
import java.util.Scanner;

public class Input {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.println("please provide some input");

        System.out.println(input.next());
    }
}
```
The given program will take input from the user and then output it as it is. We have used the `input.next()` method which is used to take string inputs (Character type input). There are several other methods to have inputs of various data types.

We'll see those methods in our next article while we explore various datatypes supported by java. Till then feel free to connect with me on

[Twitter](https://twitter.com/Raj_Pansuriya7) [LinkedIn](https://www.linkedin.com/in/raj-pansuriya/) [GitHub](https://github.com/Raj-Pansuriya/)