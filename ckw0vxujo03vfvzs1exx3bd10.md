## Datatypes in JAVA

## Primitive Datatypes
Primitive data types in Java are predefined by the Java language and named as the reserved keywords. A primitive data type does not share a state with other primitive values. Primitives are also the data types that one cannot break any further. For example, `Raj` is a data of `String` type. We can further break it into individual letters `R`, `a`, and `j` that are further unbreakable into any standalone datatype. All of the individual letters are said to be of `char` datatype. So the `String` is a `non-primitive datatype` and `char` is a primitive datatype.

Let's look at all the primitive data types supported by Java.

**Note:-** All the statements in Java language are ended by a colon ( `;` ) symbol stating that the current statement ends and a new statement begins from that point onwards.

1. __char:__ Used to store a single character or letter
```
char letter = 'r';
```
2. __int__: Used to store integers.
```
int roll_no = 10;
```
3. __long:__ Used to store large integer values
```
long large_integer = 198732099873L;
```
4. __float:__ Used to store decimal numbers
```
float marks = 77.5f;
```
5. __double:__ Used to store large decimal numbers
```
double large_decimal = 8172612.769832;
```
6. __boolean:__ The data types that have either `true` or `false` values. Very useful while writing conditional statements.
```
bool check = true;
bool var = false;
```

Also notice that the syntax to declare variables is as given in the above example.
```
datatype identifier = literal;
```
__literal:__ These are the syntactical representation of our data. In very simple language these are the actual values of our variables

__identifier:__ Name of variable, classes, methods, function are all known as an identifier. So when we declare a variable, a variable name is an identifier

Now one might wonder if we have `int`, what's the need of `long` datatype. The same goes with `float` and `double`; this has to do with the size of a datatype. An integer takes 4 bytes of memory so anything bigger than that has to be stored in a `long` type data and the same is for float. 
#### IMP
- All the decimal values by default are of type double. So if we want to store them in float type variable, we have to specify that by using an `f` at the end of our number.
- All the integer values by default are of type `int`. The only reason to use long instead of int is to store larger values. We specify that by using `L` at the end of the number.

Do not worry much about these things now. We will study everything about size when we'll be discussing bitwise operators.

## Inputs for various data types
As there are different data types, there are different methods given by the `Scanner` class to take their inputs.
- `int` : `nextInt()`
- `float` : `nextFloat()`
- `String` : `next()` is used to take _one-word_ inputs and `nextLine()` is used to take input more than a word.
for exmaple if the input given is `Hey Raj!!`, only `Hey` will be taken if `next()` is used and complete input will be taken if `nextLine()` is used. Baiscally `next()` method ignores anything after first white space.

Below is a basic program demonstrating inputs we discussed so far.

```
import java.util.Scanner;

public class Input {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Enter your full name: ");
        String full_name = input.nextLine();
        System.out.print("Enter your first name: ");
        String name = input.next();
        System.out.print("Enter your division: ");
        String division = input.next();
        System.out.print("Enter your roll no: ");
        int rollno = input.nextInt();
        System.out.print("Enter your maths marks: ");
        float marks = input.nextFloat();

        System.out.print("Name : "+full_name);
        System.out.print("Division : "+division);
        System.out.print("Roll no. : "+rollno);
        System.out.print("Marks : "+marks);
    }
}
```
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1636986829111/kKheP3fVW.png)

## Type Conversion & Casting
If you try to enter an integer or float in a string-type variable you will get an error and the program will fail. The same is true when you enter a float to an int-type variable. On the other hand, if you provide an integer to float-type data, the integer automatically gets converted to float.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1636986969600/2BCg8TD4w.png)

As you can see, in the above picture though the input given is `89` it gets converted to `89.0`. Why does this happen? And why the reverse is not possible? Why do we get an error when given a `float` to an `int` type variable?

All of this can be understood by learning about type conversion and casting.

### Conditions for Type Conversion
1. Two types should be compatible
    - `char` & `String`
    - `int` & `float`
2. Destination type should be greater than source type
    - `float` is greater than `int` cause in addition to integers it also contains decimal numbers.
    
    ![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1636987816952/ELZr6M7x4.png)
    Due to this condition, `float` does not get converted to `int`

In some situations, we might want to convert all our data into a particular datatype which we can do explicitly. This is known as Type-casting.

For example, if we want all our data in `int` type by default and we want our program to tackle the condition where a user might input a float number. then we can convert the input number into integer explicitly using the following instruction
```
int num = (int)(input.nextFloat)
```
Now even if the user inputs a float number it will be accepted without any error because we have used the `nextFloat()` method instead of `nextInt()`. It will then be converted to integer type as our code demands.

Example,
```
int num = (int)(1323.79f)
System.out.println(num)

output:
1323
```
This was all about Typecasting and data types. Have a look at the git repo below to start with some basic programs and try to understand and run them. 

%[https://github.com/Raj-Pansuriya/java-dsa/]

Change the program and play with them. You can always connect with me in case you have any doubts

[Twitter](https://twitter.com/Raj_Pansuriya7) [LinkedIn](https://www.linkedin.com/in/raj-pansuriya/) [GitHub](https://github.com/Raj-Pansuriya/)                                                 
