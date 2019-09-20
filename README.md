## The Problem

JavaScript has two visually similar,yet very different, ways to test equality. <br>
You can test equality with `==` or `===`. Here are the differences:

## Triple Equals

When using triple equals `===` in JavaScript, we are testing for **strict** equality. This means both the **type** and the **value** we are comparing have to be the same.

Lets look at a couple examples of strict equality. 

In this first example we're comparing the *number* 5 with the *number* 5. Both are **numbers**, and both share the same **value** of 5.

`5 === 5` <br>
`//true`

With this in mind, we can look more examples that will return `true`:

` 'hello world' === 'hello world'`<br>
`// true (Both **Strings**, equal **values**)` <br>

`true === true` <br>
`// true( Both **Booleans**, equal **values**)`<br>

Now lets take a look at some examples that will return `false`:

In this example we'll compare the *number* 77 to the *string value* of 77. This means our operands will have the **same value**, but a **different value**. This will return `false`

`77 === '77'`<br>
`//false ( Number vs String )`