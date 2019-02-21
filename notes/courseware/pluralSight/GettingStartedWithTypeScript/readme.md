

# Pre-requisites



## Install an IDE

Visual Studio Code is recommended to use it

[Visual Studio Code](https://code.visualstudio.com)

## Installing TypeScript

Install from the official website

This step could apply to only download an editor

[TypeScript webpage](https://www.typescriptlang.org)

### Install from the CMD

```bash
npm install -g typescript

```

| This installation must be performed in the root folder of the project MultiMath previously downloaded

## Install nodeJS

Install from the official website

[nodeJS](https://nodejs.org)



# What is TypeScript

## TypeScript

- Open source
- Maintained by Microsoft
- Transpiles to a configurable JavaScript version
- Uses ES6/ES7 sintax if possible
- Adds typing

### Benefits of a typed language

- Mistakes are detected up front
- Less bugs
- Autocomplete/Intellisense
- Makes endless type checking unnecesary
-  Bottom line: it saves you a lot of time



## The compiler

The `TypeScript` compiler is called `tsc` (type script compiler), it convert TypeScript code to JavaScript.

The browsers does not understand TypeScript code, the compiler is available in many OS such as windows, mac and Linux.



# Coding

## Ending line

In TypeScript is optional to end each line with a `;`

## Data types

The first data type is the ones that comes with TypeScript

| Built-in | Comment                                                      |
| -------- | ------------------------------------------------------------ |
| boolean  | can contains true o false value                              |
| string   | can contains a sequence of characters surrounded by quotes   |
| number   | any type of number such as int, float, double, negative, positive etc. |
|          |                                                              |

The second data type is the created by the developer

| Custom    | Comment |
| --------- | ------- |
| enum      |         |
| array     |         |
| interface |         |
| class     |         |
|           |         |

## Naming conviction

### Class

The naming conviction for class is PascalCase

### Methods or functions

The naming conviction for methods or functions is camelCase



## Class structure

```typescript
class SomeClass {
    // code here
}
```

## Class atributtes

```typescript
variableName: typeOfVariable = <value>;
```



## Method or function structure

```
someMethod(): returnTypeValue {
    // code here
}
```

### Reference to class atributtes

```
this.variableName
```

| To refere to some global attribute on the class level we have to use `this`  *keyword*

## Variables

| In TypeScript every variable is assing to a data type unlike to JavaScript where you can assing any type to every variable you declare

```typescript
var notSure: any = 4;
notSure = "maybe a string instead";
notSure = false;
```

## Type inference

### Variables

| TypeScript wont let you `reassignment of variables` of different type, e.g:

#### Explicitly

```
var number: value = .25; // define and initialize the variable
number = "String"; // the error you will get: type "String" is not assignable to type number
```

#### Implicitly

```typescript
value = .25; // define and initialize the variable
number = "String"; // the error you will get: type "String" is not assignable to type number
```

### Methods or functions

The same can be applied to `methods or functions`, e.g:

#### Explicitly

```typescript
methodName(): string {
    return "String"
}
```

#### Implicitly

```typescript
methodName(): {
    return "String"
}
```





