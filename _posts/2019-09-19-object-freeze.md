---
published: false
---
## More than CONST

There is one big pitfall with const.

When we say "`const` variables are immutable" it only means that the variable always has to point to the same thing. It does not mean than the thing it points to can’t change over time.

For example, if the variable foo is a const that points to an object — we can’t make foo point to another object later on:

```JavaScript
const foo = {};
foo = {}; // TypeError: Assignment to constant variable.
```
But we can however mutate, make changes to, the object foo points to, like so:

```JavaScript
const foo = {};
foo['prop'] = "Moo"; // This works!
console.log(foo);
```
If we want the value of foo to be immutable we have to freeze it using Object.freeze(…​).

### Resource
https://codecraft.tv/courses/angular/es6-typescript/const/
