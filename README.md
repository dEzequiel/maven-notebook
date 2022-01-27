# Maven notebook

## Quick topics

Maven is a standard tool used for building and managing any Java-based project.

Maven buils projects using what's called *project object model (POM)* an XML file that contains information about the project and configuration details used by Maven to build the project. When executing a task or goal, Maven looks for the POM in the current directory. It reads the POM, gets the needed configuration information, then executes the goal.

Maven provides guidelines for best practices development, in one of the most importants topics, tests. Maven keeps tests code in separate from source code, use test naming conventions to find tests and having test cases setup environment.

# Install Maven
**You must have Java installed in order to proceed.**

[Download](https://maven.apache.org/download.cgi)

**Ubuntu 20.04**

``` 
sudo apt get install maven 
```

Next command should print installed Maven version
```
mvn -v
```
```
Maven home: /usr/share/maven
Java version: 1.8.0_312, vendor: Private Build, runtime: /usr/lib/jvm/java-8-openjdk-amd64/jre
Default locale: es_ES, platform encoding: UTF-8
OS name: "linux", version: "5.4.0-96-generic", arch: "amd64", family: "unix"
```

# Create a project

- Quick topics
  - **Archetype** is the exemplpary pattern from which other objects, ideas, or concepts are derived. In few words, is the perfect model.

Create a folder and move into that folder, then open a terminal
```
mkdir my-folder
cd my-folder
```

Execute the following Maven instruction. *Change it by your preferences*.
```
mvn archetype:generate -DgroupId=com.mycompany.app -DartifactId=my-app -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4 -DinteractiveMode=false
```
*Archetype* is just a plugin that contains a collection of goals with a general common purpose. It just creates a simple project based upon a **maven-archetype-quickstart archetype**.

A new directory with the **artifactId** attribute name defined its created, move into that file and you will see basic Maven project structure.

```
maven-notebook-project
|-- pom.xml
`-- src
    |-- main
    |   `-- java
    |       `-- com
    |           `-- mycompany
    |               `-- app
    |                   `-- App.java
    `-- test
        `-- java
            `-- com
                `-- mycompany
                    `-- app
                        `-- AppTest.java
```

The ```src/main/java``` directory contains the project source code, the ```src/test/java``` directory contains the test source, and the ```pom.xml``` file is the project's Project Object Model, or POM.