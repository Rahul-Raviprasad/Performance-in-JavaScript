### Native Methods

#### 1. Always choose Native methods over writing your own code.
No matter how optimal your JavaScript code is, it will never be faster than the native methods provided by the JavaScript engine. The reason for this is simple: the native parts of JavaScript—those already present in the browser before you write a line of code—are all written in a lower-level language such as C++. That means these methods are compiled down to machine code as part of the browser and therefore don’t have the same limitations as your JavaScript code.

Example : the Selectors API, which allows querying of a DOM document using CSS selectors.
![MDN](https://developer.mozilla.org/en-US/docs/Web/API/Document_object_model/Locating_DOM_elements_using_selectors)
![Selectors API Level 2](https://www.w3.org/TR/selectors-api2/)
