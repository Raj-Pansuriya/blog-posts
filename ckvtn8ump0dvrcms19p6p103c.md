## Introduction to Java

In previous articles, we discussed that we write all our code in a human-readable format. We also got to know that computers can only understand machine language i.e., the language of 0's & 1's. We know that there is an intermediate agent known as a compiler that translates human-readable code to machine-readable code.

In this article, we'll be exploring more about compiler (Java compiler in depth). We'll look into the basic building blocks of java, how a java code executes, the basics of java language, how everything works internally from writing a java code to its execution, what are the different components of the java compiler, and so on.

While exploring our computer storage, one might observe that different types of files possess different extensions. a PowerPoint file have .pptx extension, a doc file have .docx extension, a pdf file have .pdf file extension, a picture may have .jpg/.png extension etc. In the same way, a java file will have a __.java__ extension.

So the .java file will contain all our code in human-readable form. The code might be any set of instructions as per rules (syntax) of the Java language.

## How JAVA is Platform Independent
In some programming languages such as C, C++ the compiler converts the .c or .cpp file directly into machine code giving us a .exe file that is platform dependent. If we try to execute such a .exe file on a different Operating System (OS) than what it was created on, we won't be able to do so. Once the type of OS is changed, the code needs to be re-compiled. This means a c/c++ code compiled on windows will not execute on a Linux OS or a MAC OS and vice-versa.

Unlike those programming languages, when a java compiler compiles a .java file, it converts it into something known as __byte code__. Some important points about byte code are:
- This code file will have _.class_ extension
- This code will still not be understood by a computer, which means it won't directly run on a system
- We'll need something called Java Virtual Machine (JVM) to execute this code

Now one might have so many different questions such as what is byte code? Why do we have a byte code? What is JVM? What does JVM do? How does all of this relate to the platform independence of JAVA? etc. Let's answer all of them one by one.

Consider byte code as some intermediate language of java. Java Virtual Machine acts as an interpreter for byte code. That means when the byte code is run by JVM, it gets converted to machine code and hence is finally ready to be executed.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1636539931785/XaPY_GW3s.png)

The byte code once compiled, can be used to generate machine code on all types of operating systems. Say a byte code is generated on macOS, we can still use that byte code to generate machine code on Linux/Windows OS. This is how Java gets its platform-independent behavior because, unlike other programming languages, we do not have to recompile the program every time we change our OS.

#### More on Platform Independence
- byte code (.class file) can run on all operating systems.
- JVM converts the byte code into machine code.
- JAVA is platform-independent, but JVM is not.

## Architecture of JAVA

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1636541833244/I5nifrMjW.png)

#### Java Development Kit (JDK)
- Provides an environment to develop and run Java programs
- It is a package that consists of :
    1. Development tools: Provide an environment to develop a java program
    2. Java Runtime Environment (JRE): to execute java programs
    3. A compiler __javac__: Converts java code into byte code. ( .java -> .class )
    4. Archiver __jar__: If we want to archive our files
    5. Docs generator __javadoc__: to generate docs of our application
    6. interpreter & loader
- In short, if we want to write and develop java codes, we need to have JDK

#### Java Runtime Environment (JRE)
- It is a package that provides an environment to _only run_ the java programs
- It consists of :
    1. Deployment Technologies
    2. User Interface toolkits
    3. Integration Libraries
    4. Base libraries
    5. JVM
- After we get the byte code ( .class file ), at run time:
    1. loader loads all the necessary classes needed to execute the program.
    2. JVM sends code to _byte code verifier_ to check the format of the code.

#### Compile Time

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1636550710827/rlEBpPKAY.png)

During compile-time, the source code written by us ( .java file) is coverted t byte code ( .class file) by java compiler (javac).

#### Run Time

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1636550875244/cO-n5RzrY.png)

Most of the runtime period is dominated by __JVM__ and its components.

###### __Class loader (Working of JVM)__
1. Loading :
    - Reads .class file and generate binary data in form of object
    - The object of .class is generated in heap memory. The object contains source code, necessary data, any other necessary java libraries which we may have referenced in our code, etc.
    - In simple terms, we can say that the program is loaded in the RAM of the computer in the loading process

2. Linking :
    - JVM verifies the .class file to avoid any errors/any things prohibited by Java
    - Allocates memory for class variables & default values because all the variables, constants, functions, methods, etc. needs to be allocated the proper amount of memory in RAM
    - Replace all the symbolic references with direct references.
for example, if our code has a statements
```
a = 10
b = 20
c = a + b
```
then `a` has to be replaced with 10, `b` with 20, and `c` with 10+20.

3. Initialization :
    - All static variable are assigned their values defined in the code and static block.
We'll be seeing static variables in detail in our further articles when we'll discuss OOP. For now, understand static variables as variables that are independent of the object of the class.

Now that we have source code, data, and other libraries properly loaded, verified, and linked; it's time to generate machine code from that.

###### __JVM Execution__
1. Interpreter :
    - Line by line execution of .class file

    Note: Because the interpreter interprets the byte code line-by-line, it will read and interpret any function or variable over and over again if every time it's called. That means a function is converted to machine code every time it's used in source code, which is not really efficient. To solve this problem we have, Just in Time compiler ( JIT ).

2. Just In Time Compiler ( JIT ) :
    - JIT provides direct machine code for methods that are repeated in source code to avoid re-interpretation
    - Makes execution faster

#### JRE vs JVM
Think of JRE as a box and JVM as the content inside the box, the main working machine being JVM. JVM does all the necessary processing on source code but the things which JVM might require such as dependent libraries, base libraries in order to do that procession are held and provided by JRE. Whenever JVM needs any help, its main point of contact is JRE.

We can say that `JRE = JVM + some other files & tools`

#### Collectively

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1636555326553/37XAWqZRv.png)
- We write java code in human-readable form
- Compiler javac inside JDK compiles it to form a .class file of byte code
- JVM runs and the byte code and give us an executable code which is then run via JRE

#### Reference


%[https://www.youtube.com/watch?v=4EP8YzcN0hQ&list=PL9gnSGHSqcnr_DxHsP7AW9ftq0AtAyYqJ&index=3]


In next article, we'll start with our `Hello World` Java code. Till then feel free to connect with me on my socials!!!