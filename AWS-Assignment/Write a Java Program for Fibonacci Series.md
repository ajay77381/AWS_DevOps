# What is Java ?

Java is a programming language and a platform. Java is a high level, robust, object-oriented and secure programming language.

Java was developed by Sun Microsystems (which is now the subsidiary of Oracle) in the year 1995. James Gosling is known as the father of Java. Before Java, its name was Oak. Since Oak was already a registered company, so James Gosling and his team changed the name from Oak to Java.

**Platform**: Any hardware or software environment in which a program runs, is known as a platform. Since Java has a runtime environment (JRE) and API, it is called a platform.

Java Example
Let's have a quick look at Java programming example. A detailed description of Hello Java example is available in next page
`````````````````````````````
class Simple{  
    public static void main(String args[]){  
     System.out.println("Hello Java");  
    }  
} 
`````````````````````````````````````````

# Fibonacci Series In Java
Reference url - https://logicmojo.com/fibonacci-series-in-Java



![Image](https://github.com/user-attachments/assets/ca4b19ac-e416-4555-93d3-943e1e42c827)

𝑻𝒂𝒃𝒍𝒆 𝒐𝒇 𝑪𝒐𝒏𝒕𝒆𝒏𝒕****

[Introduction](https://logicmojo.com/fibonacci-series-in-Java#intro)
[What Is Fibonacci Series In Java?](https://logicmojo.com/fibonacci-series-in-Java#WhatIsFibonacci)

[First Program :- Fibonacci Series in Java using For Loop](https://logicmojo.com/fibonacci-series-in-Java#FibonacciSeriesinJava)
[Second Program :- Fibonacci Series in Java using While Loop](https://logicmojo.com/fibonacci-series-in-Java#usingWhileLoop)



Introduction

The Fibonacci Series is a type of sequence that begins with 0 and 1 and continues with numbers that are the sum of the two previous numbers. The Fibonacci series in Java is a program that returns a Fibonacci Series of N numbers when provided an integer input N. Before beginning to code, it is critical to grasp the Fibonacci Series and the logic required to solve the problem.

What Is Fibonacci Series In Java?

In Java, a Fibonacci series is a sequence of numbers in which every third number equals the sum of the preceding two numbers. The fibonacci series' first two integers are 0 and 1.

The Fibonacci Series Looks like this :
`````````````````````````````````````````````````````````
 0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89.............         
`````````````````````````````````````````````````````````````````````



![Image](https://github.com/user-attachments/assets/97b92f3b-dc07-4333-af2a-a64d5c954506)



![Image](https://github.com/user-attachments/assets/ef2d9795-db21-40d6-8b02-7e0bb9925e68)

Example

Print the Fibonacci Series up to the N term for a specified input integer N.

````````````````````````
input= 13

output= 0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144,           
```````````````````````````````````
Because we interpreted the first Fibonacci term as 0 and the second as 1, the term becomes the sum of the first and second integers, which is 1.

There are different ways or methods to display the Fibonacci series.


# First Program :- Fibonacci Series in Java using For Loop-

This loop is identical to the while loop. After initializing the first two digits, we print the first term of the sequence, thus computing the next term using the Fibonacci formula. Finally, proceed by giving the value of the second term to the first term and the value of the next term to the second term.

````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````
class Main {
  public static void main(String[] args) {

    int n = 13, t1 = 0, t2 = 1;
    System.out.println("Fibonacci Series of " + n + " terms:");

    for (int i = 1; i <= n; ++i) {
      System.out.print(t1 + ", ");

      // compute the next term
      int sum = t1 + t2;
      t1 = t2;
      t2 = sum;
    }
  }
}
````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````

## Output-

````
Fibonacci Series of 13 terms:
0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144,

`````

In the preceding code, firstTerm(t1) and secondTerm(t2) are set to 0 and 1, respectively. (first two digits of Fibonacci series). In this case, we used the for loop to print the t1 of the series calculate sum by adding t1 and t2 and give the value of t2 to t1 and sum to t2.



# Creating a Project


Installation

Maven is a Java tool, so you must have [Java](https://www.oracle.com/technetwork/java/javase/downloads/index.html) installed in order to proceed.
After that, type the following in a terminal or in a command prompt:


mvn --version

It should print out your installed version of Maven, for example:

ajay@DESKTOP-M8NEQM2:~/aws/fibo$ mvn --version
Apache Maven 3.9.5 (57804ffe001d7215b5e7bcb531cf83df38f93546)
Maven home: /home/ajay/.sdkman/candidates/maven/current
Java version: 21.0.2, vendor: Oracle Corporation, runtime: /home/ajay/.sdkman/candidates/java/21.0.2-open
Default locale: en, platform encoding: UTF-8
OS name: "linux", version: "5.15.153.1-microsoft-standard-wsl2", arch: "amd64", family: "unix"




1- Depending upon your network setup, you may require extra configuration. Check out the [Guide to Configuring Maven](https://maven.apache.org/guides/mini/guide-configuring-maven.html) if necessary.

If you are using Windows, you should look at [Windows Prerequisites](https://maven.apache.org/guides/getting-started/windows-prerequisites.html) to ensure that you are prepared to use Maven on Windows.

# You need somewhere for your project to reside. Create a directory somewhere and start a shell in that directory. On your command line, execute the following Maven goal:
Example- i created the directory **fibo** and runed the below command:

````
mvn archetype:generate -DgroupId=com.ajay -DartifactId=fibbo-app -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false
`````

ls -l
cd fibbo-app/
 ls -la
git init
 git status
 git add .
git commit -m "initial checking"
 git remote add origin git@github.com:ajay77381/fibbo-app.git
git push origin main


Note- If we want to remove the remote connection then we can user git remote remove command like following-

`` git remote remove origin
``

How to Create ssh key for your git hub profile and add in git hub ?

Use below command to generate the ssh key- 
cd ~/.ssh
  ls -la
  ssh-keygen
  cat id_rsa.pub

Click on the Setting-


![Image](https://github.com/user-attachments/assets/68f6e8b3-0545-44a3-bd8a-a9a3bf4e0323)

Then click on **SSH and GPG keys**

![Image](https://github.com/user-attachments/assets/80877473-82b8-4ccf-ba52-cd349778fe94)

and click on create new ssh key then paste the created ssk key-



![Image](https://github.com/user-attachments/assets/fd576ebb-7f8c-4705-b532-8d3effae2974)

mvn clean install
java -jar target/fibbo-app-1.0-SNAPSHOT.jar



![Image](https://github.com/user-attachments/assets/a3a2dbb1-dbd6-4245-b446-2730c5b4627b)
















