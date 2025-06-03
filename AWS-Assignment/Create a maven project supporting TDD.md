

## What is Maven ?

Maven was created to provide a standard way in which Projects can be built. One of its powerful features is dependency management.

Maven is commonly used for dependency management, but it is not the only thing it is capable of doing.

## What is pom.xml ?
POM stands for Project Object Model. pom.xml has all the details about your project, and this is where you will tell maven what it should do.

# How to Create a maven project supporting TDD ?

1- I create the directory in d rive by the name dev and  git clone **https://github.com/ajay77381/java_tdd_maven.git**

2- I set up the Local Java version manager using the below step- 

`
curl -s "https://get.sdkman.io" | bash
`
Follow the on-screen instructions to wrap up the installation. Afterward, open a new terminal or run the following in the same shell-
 source "$HOME/.sdkman/bin/sdkman-init.sh"


Lastly, run the following snippet to confirm the installation's success:
$ sdk version

You should see output containing the latest script and native versions:

SDKMAN!
script: 5.18.2
native: 0.4.6

sdk list java



Now install the required version of java from the given list-

openjdk version "21.0.2" 2024-01-16

java -version


Now go inside the directory cd java_tdd_maven/ and install maven using the below command-

```
sdk install maven 3.9.5
```
 mvn clean spring-boot:run



> mvn clean install

>  java -jar target/baby-0.0.1-SNAPSHOT.war


