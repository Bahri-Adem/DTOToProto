# JavaToProto

## Overview

The `JavaToProto` class is a utility for generating Protocol Buffer Specification files from Plain Old Java Objects (POJOs). This class takes a POJO as input and creates the associated Proto Buffer Specification File. It supports various features like nested POJOs, enums, arrays, collections, maps, primitives, and boxed primitives.

## License

This class is licensed under the Public Domain. You are free to use, modify, and distribute it as you wish. However, the original author asks that if you find bugs or improve the code, you contribute by raising a pull request or an issue.

## Usage

### Command Line Interface (CLI)

```bash
java -jar JavaToProto.jar JavaToProto <class name> [<output file name>]
```
- If the output file name is not specified, the output will be printed to the console.
- Ensure that the class name is in the classpath somewhere.

### Code Integration

```java
JavaToProto jpt = new JavaToProto(className);
String protoFile = jpt.toString();
```
- Replace className with the name of the class you want to generate a Proto file for.
This will return the Proto file as a string.
### Features
- Supports nested POJOs, enums, arrays, collections, maps, primitives, and boxed primitives.
- Does not support nested collections or arrays with more than one dimension.
### How It Works
- The main method serves as the entry point for CLI usage.
- The JavaToProto class takes a POJO class as input and processes its fields to generate the Proto file.
- It utilizes reflection to analyze the structure of the provided class and generate corresponding Proto message definitions.
- Enums, arrays, collections, and maps are handled recursively to generate nested message definitions when necessary.
### Contributions
- Contributions to improve this utility or fix any bugs are welcome. Please raise a pull request or an issue on the repository.

### Disclaimer
- The author of this class is not responsible for any usage of the code or any resulting bugs or issues. Use it at your own discretion.
