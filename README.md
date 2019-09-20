## The Problem

JavaScript has two visually similar,yet very different, ways to test equality. <br>
You can test equality with ### `==` or ### `===`. Here are the differences:

## Triple Equals

When using triple equals ### `===` in JavaScript, we are testing for **strict** equality. This means both the **type** and the **value** we are comparing have to be the same.

Lets look at a couple examples of strict equality. 

In this first example we're comparing the *number* 5 with the *number* 5. Both are **numbers**, and both share the same **value** of 5.

`5 === 5`
`//true`