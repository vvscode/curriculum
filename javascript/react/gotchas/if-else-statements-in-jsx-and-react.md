---
author: catalin

levels:
  - basic
  - beginner

type: normal

category: how to

links:
  - '[facebook.github.io](https://facebook.github.io/react/tips/if-else-in-JSX.html){website}'

parent: custom-proptype-s-to-be-required

---
# if/else statements in **JSX** and **React**

---
## Content

**JSX** is a JavaScript extension intended to be a syntactic sugar for function calls and object construction.

Due to this, `if-else` statements won't work inside **JSX** as they would translate as the following:

```jsx
<div id={if (condition){'msg'}}> Hello</div>
// will translate into:
React.createElement("div",
{id: if (condition) { 'msg' }}, "Hello");
```

Instead, ternary expressions can be used:

```jsx
<div id={condition ?'msg':null}> Hello</div>
```

If ternary expressions are too convoluted, an `if-else` statement can be used outside the **JSX** to determine what components to use.

Another alternative is that *immediately-invoked function expressions* can be used in-line inside **JSX**:

```jsx
<p>
  {(() => {
    switch (this.state.somestate) {
      case "one": return "enki";
      case "two" : return "enki2";
      case "three" : return "enki3";
    }
  })()}
</p>
```

---
## Practice

Can you use switch statements in JSX?

???

* only wrapped in an IIFE
* yes
* no
* only for strings

---
## Revision

How would you write `if (condition) return 'x' else return 'y'` in JSX id assignment?

```javascript
<div id=
  {
    ??? ??? ??? ??? ???
  }>
```

* condition
* ?
* 'x'
* :
* 'y'
* x
* y
* if
* else
* switch
* () =>
 
