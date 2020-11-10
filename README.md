# Javascript-jokes

A compilation of javascript expressions that returns unexpected results, hence jokes

## Array !== Array

```js
[] === []; // -> true
[] == ![]; // -> true
NaN === NaN; // -> false

true == []; // -> false
true == ![]; // -> false

false == []; // -> true
false == ![]; // -> true

!!"false" === !!"true"; // -> true
!!"false" === !!"false"; // -> true ;)

"b" + "a" + +"a" + "a"; // -> 'baNaNa'
"foo" + +"bar"; // -> 'fooNaN'


(![] + [])[+[]] +
  (![] + [])[+!+[]] +
  ([![]] + [][[]])[+!+[] + [+[]]] +
  (![] + [])[!+[] + !+[]]; // fail

!![]       // -> true
[] == true // -> false


!!null; // -> false
null == false; // -> false
0 == false; // -> true
"" == false; // -> true

//
document.all instanceof Object; // -> true
typeof document.all; // -> 'undefined'
typeof NaN; // -> 'number'


```

## funtion is not function

```js
class Foo extends null {}
// -> [Function: Foo]

new Foo() instanceof null;
// > TypeError: function is not a function
// >     at … … …
```

## Array equality is mocking you

```bash
[1, 2, 3] + [4, 5, 6]; // -> '1,2,34,5,6'

[] == ''   // -> true
[] == 0    // -> true
[''] == '' // -> true
[0] == 0   // -> true
[0] == ''  // -> false
[''] == 0  // -> true

[null] == ''      // true
[null] == 0       // true
[undefined] == '' // true
[undefined] == 0  // true

[[]] == 0  // true
[[]] == '' // true

[[[[[[]]]]]] == '' // true
[[[[[[]]]]]] == 0  // true

[[[[[[ null ]]]]]] == 0  // true
[[[[[[ null ]]]]]] == '' // true
[[[[[[ null ]]]]]] == true // true

[[[[[[ undefined ]]]]]] == 0  // true
[[[[[[ undefined ]]]]]] == '' // true
[[[[[[ undefined ]]]]]] == true // true
```

## pure function is also not pure function

```js
//
parseInt('Infinity', 10); // -> NaN
parseInt('Infinity', 18); // -> NaN...
parseInt('Infinity', 19); // -> 18
parseInt('Infinity', 23); // -> 18...
parseInt('Infinity', 24); // -> 151176378
parseInt('Infinity', 29); // -> 385849803
parseInt('Infinity', 30); // -> 13693557269
parseInt('Infinity', 34); // -> 28872273981
parseInt('Infinity', 35); // -> 1201203301724
parseInt('Infinity', 36); // -> 1461559270678...
parseInt('Infinity', 37); // -> NaN
```
