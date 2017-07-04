# Default constructors

As stated, if you do not specify a constructor method a default constructor is used. For base classes the default constructor is:

```js
constructor() {}
```

For derived classes, the default constructor is:

```js
constructor(...args) {
  super(...args);
}
```
