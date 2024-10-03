#  Goal of this project :

The aim of this project is to learn how to package an application, written in Java, as a JAR file.

The application itself prints in the terminal a small message, "Hello World" / "Goodbye World" (by default).

## How to build it _(requires Maven)_ :
1. Download the dependencies and their transitive dependencies : 
```
./mvnw dependency:go-offline
```

2. Package the application
```
./mvnw package
```
## How to use it :

To run the packaged application, you have to run in the terminal the command : 
```
java -jar target/java-intellij-idea-and-maven-1.0-SNAPSHOT.jar "name" [word] [parameters]
```


_General paramaters :_
- The field "name" replace the name of the person addressed to (default = World).
- The field [word] can either be replaced by "hello" or "goodbye".
- -h, --help : shows a help message for subcommands
- -V, --version : shows the version information

_hello [parameters] :_
- -g / --greetings "..." : replace the greetings by the word contained in " " (default = Hello)

_goodbye [parameters] :_
- -f, --farewells "..." : replace the farewells by the word contained in " " (default = Goodbye)