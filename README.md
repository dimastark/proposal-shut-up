# Shut-up Operator `@`

- [Motivation](#motivation)
- [Usage examples](#usage-examples)
- [Potential problems](#potential-problems)
- [Other languages](#other-languages)

## Motivation

We all love good old ~~Java~~ECMAScript. And we all want to write code the way our ancestors did. 
Without fear of suddenly appearing exceptions, type errors and `undefined is not a function`.

Best practices from Vanilla ES:
* There is no "division by zero error", only `Infinity`
* There is no errors in `parseInt('💩')`, only `NaN`
* There is no "reference error", only `undefined`

And that's really beautiful...

Why not generalize this practices and silence all these annoying errors? Just use "shut-up" operator `@`.

## Usage examples

No need to check input arguments.

```javascript
function f(callback) {
    callback('result');
}

// Haters gonna hate
@f(undefined);
```

No uncontrolled exceptions.

```
// Bye-bye "Cannot read property"
@(null.is.safe.now);
```

[Unlimited](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Strict_mode) power.

```javascript
'use strict';  // Pfftt, @ don't care

@(true.value = 1);
```

Just add `@`.

## Potential problems

* Conflicting syntax with [decorators](https://github.com/tc39/proposal-decorators). But who needs decorators, if you have such a feature as `@` operator.
* Maybe too powerful for mere mortals.

## Other languages

* [try?](https://docs.swift.org/swift-book/LanguageGuide/ErrorHandling.html) in [Swift](https://swift.org/)
* [@](https://www.php.net/manual/en/language.operators.errorcontrol.php) in [PHP](https://www.php.net/)
