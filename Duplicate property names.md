# Duplicate property names

When using the same name for your properties, the second property will overwrite the first.

```js

var a = {x: 1, x: 2};
console.log(a); // {x: 2}

```

In ECMAScript 5 strict mode code, duplicate property names were considered a `SyntaxError`.  With the introduction of *computed property names* making duplication possible at runtime, ECMAScript 2015 has removed this restriction.

```js

function haveES2015DuplicatePropertySemantics() {
  'use strict';
  try {
    ({prop: 1, prop: 2});
    // No error thrown, duplicate property names allowed in strict mode
    return true;
  } catch(e) {
    // Error thrown, duplicates prohibited in strict mode
    return false;
  }
}

```

[Source](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Operators/Object_initializer#Duplicate_property_names)

From ES spec [Annex E](http://www.ecma-international.org/ecma-262/6.0/#sec-additions-and-changes-that-introduce-incompatibilities-with-prior-editions):

In ECMAScript 2015, it is no longer an early error to have duplicate property names in Object Initializers.

