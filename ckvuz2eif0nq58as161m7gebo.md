## Getting Started with JAVA

You can install the latest version of java for Windows and macOS from its official site. For Linux-based distributions command line is the recommended option. Follow the instructions:
- Install java for [MacOS](https://www.oracle.com/java/technologies/downloads/#jdk17-mac)
- Install java for [Windows](https://www.oracle.com/java/technologies/downloads/#jdk17-windows)
- Install java for [linux](https://www.oracle.com/java/technologies/downloads/#jdk17-linux)
Note: Though you can download and install JDK for Linux from the official site, I would highly recommend you to use the official package manager for your distribution.

#### Java on Linux distributions
- Ubuntu, Debian, and distributions that use **apt** as the package manager
    Open your terminal and follow the guide

    Update the package index
    ```
    $ sudo apt-get update
    ```
    Check if Java is not already installed:
    ```
    $ java --version
    ```
    If Java is already installed we'll get output similar to below
    ```
    openjdk 17.0.1 2021-10-19
    OpenJDK Runtime Environment (build 17.0.1+12)
    OpenJDK 64-Bit Server VM (build 17.0.1+12, mixed mode)
    ```
    If not, then install java
    ```
    $ sudo apt-get install default-jdk
    ```
- For arch and arch-based distributions

    Update the system
    ```
    $ sudo pacman -Syyu
    ```
    Check if Java is not already installed:
    ```
    $ java --version
    ```
    Search for available JRE in the arch repository
    ```
    $ pacman -Ss java | grep jre
    ```
    ![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1636607547791/t-klDRH8W.png)
    Install the latest jre
    ```
    $ sudo pacman -S jre-openjdk
    ```
    Similarly, search for the latest JDK and install it
    ```
    $ pacman -Ss java | grep jdk
    ```
    ![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1636607674128/WRL8RwQJ4.png)
    ```
    $ sudo pacman -S jdk-openjdk
    ```
The next thing you may want to install is an Integrated Development Environment (IDE). There are so many IDE's available for Java development. One of the best being [IntelliJ IDEA](https://www.jetbrains.com/idea/download). You may even consider setting a Java Development Environment in your preferred text editor such as [VSCode](https://code.visualstudio.com/) or [Atom](https://atom.io/), etc. I leave these things to your liking.

That's all for this one. Feel free to connect with me
[![Twitter logo](https://img.shields.io/badge/Twitter-Profile-informational?style=flat&logo=twitter&logoColor=white&color=1CA2F1)](https://twitter.com/Raj_Pansuriya7)

[![LinkedIn Badge](https://img.shields.io/badge/LinkedIn-Profile-informational?style=flat&logo=linkedin&logoColor=white&color=0D76A8)](https://www.linkedin.com/in/raj-pansuriya/)