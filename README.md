# OCL Compiler to Javascript for NodeMDA
## Introduction
This project is a Node package that implements **OCL Compiler** generating code into JavaScript. **OCL** acronym 
stands for **Object Constraint Language** which is a query language used to impose constraints on UML model
elements. The purpose of this package is to generate code into JavasScript to ensure that the constraints, which were modeled in a UML diagram, are fulfilled at runtime.

This package is not meant for a stand-alone use because it is tightly binded to the 
[**NodeMDA**](https://www.npmjs.com/package/nodemda) code-generation engine developed by Joel Kozikowski.

## Installation
First you need to install **NodeMDA** code-generation engine. The process is well-described at 
[**NodeMDA help page**](https://www.npmjs.com/package/nodemda).

**_Command line_**
```
npm install -g nodemda-ocl-to-js
```

## Usage
At first, you need to setup a project as it is again described at [**NodeMDA help page**](https://www.npmjs.com/package/nodemda).

Then create some files with **ocl** extension inside the project directory. You can structure your **OCL files**
into subdirectories as you wish, the OCL compiler will find them.

**_Then run command:_**
```
nodemda gen --platform ocl-to-js
```
**Please note that the current release is in pre-alpha version. The OCL compiler does not follow OCL standard in all details yet.**

## Supported OCL language features
* Context and Package declarations
* Navigation statements around a UML model
* Supported OCL constraints: **inv, pre, post**
* Most OCL operators
* Most functions for primitive types
* Most functions for collection types

## The JS libraries this package is using
* [PegJS parser generator](http://pegjs.majda.cz)
* [Handlebars templating engine](https://www.npmjs.com/package/handlebars)
* [JS code beautifier](https://www.npmjs.com/package/js-beautify)
* [Winston logger](https://github.com/winstonjs/winston)