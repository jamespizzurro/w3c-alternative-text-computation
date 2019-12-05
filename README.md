W3C Accessible Name Computation Prototype
A functional prototype for the W3C Alternative Text Computation.

The Accessible Name Computation Prototype
-----

To ensure interoperability, the W3C Alternative Text Computation must be supported in all browsers equally.

The AccName Prototype mirrors the development of the W3C AccName specification, which will be updated accordingly with all expected behaviors as this development continues within the W3C ARIA Working Group.
http://www.w3.org/TR/accname-aam-1.1/

Live AccName Prototype Test Page
https://whatsock.github.io/w3c-alternative-text-computation/Editable%20Live%20Input%20AccName%20Test.html

How To Import
-----

The AccName Prototype algorithm code is contained in the file "recursion.js" in the folder "docs/Sample JavaScript Recursion Algorithm", which can be remotely loaded into any project using JavaScript like so.

```
<script type="text/javascript" src="https://whatsock.github.io/w3c-alternative-text-computation/Sample%20JavaScript%20Recursion%20Algorithm/recursion.js"></script>
```

Or the same, but compressed for faster loading.

```
<script type="text/javascript" src="https://whatsock.github.io/w3c-alternative-text-computation/Sample%20JavaScript%20Recursion%20Algorithm/recursion.min.js"></script>
```

The recursion.js file can also be imported directly into React projects using the following syntax:

```
require("./path/recursion.js");
```

An example of this, is included within the React project at
https://github.com/whatsock/bootstrap-react
(Within the file: "src\AccDC\Core\API.js")

General Usage
-----

```
  var props = getAccName(elementNode); // Generate the Name and Description properties of an element. ( props.name and props.desc )
```

```
alert(props.name); // Show accessible Name property
```

```
alert(props.desc); // Show accessible Description property
```

```
alert(props.placeholder); // Show boolean true or false if accessible name was computed from placeholder alone.
```

```
alert(props.userAgent); // Show boolean true or false if accessible name was computed from user agent alone.
```

```
alert(props.error); // Show error if one is generated. 
```

The props.error property only populates if the code throws a syntax error. (These should always be reported here as a new issue when discovered.
https://github.com/whatsock/w3c-alternative-text-computation/issues )

Callback Usage
-----

```
getAccName( elementNode, function( props, rootNode ) {
    alert(props.name); // Show accessible Name property for rootNode
    alert(props.desc); // Show accessible Description property for rootNode
    alert(props.error); // Show error if one is generated.  
});
```

Testable Statements
-----

The W3C Testable Statements Generator script is included, which will automatically generate executable HTML files of all of the testable statements at
https://www.w3.org/wiki/AccName_1.1_Testable_Statements

Which also automatically generates the following index.html file in the output folder for testing on webservers.
https://whatsock.github.io/w3c-alternative-text-computation/Autogenerated%20AccName%201.1%20Testable%20Statements%20-%20W3C/index.html

Distributed under the terms of the Open Source Initiative OSI - MIT License.

Developed and maintained by: Bryan Garaventa https://www.linkedin.com/in/bgaraventa
Or on Twitter at https://twitter.com/bryanegaraventa

Includes additional contributions by members of the W3C ARIA Working Group.

Related projects:
-----

* WhatSock Organization: https://github.com/whatsock
* Visual ARIA: https://github.com/accdc/visual-aria
