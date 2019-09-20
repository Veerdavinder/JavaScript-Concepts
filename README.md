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
`// true( Both `**Booleans**`, equal `**values**`)`<br>

Now lets take a look at some examples that will return `false`:

In this example we'll compare the *number* 77 to the *string value* of 77. This means our operands will have the **same value**, but a **different value**. This will return `false`

`77 === '77'`<br>
`//false ( Number vs String )`

Again, the key takeaway for triple(strict) equality is that both the **type** and the **value** we are comparing have to be the same.

## Double Equals

When using double equals in JavaScript we are testing for **Loose equality**. Double Equals also performs **type coercion**.

`Type coercion means that two values are compared only after attempting to convert them into a common type.`
An example will illustrate this. Recall earlier when we tested the following with strict equality:

`77 === '77'`<br>
`// false (Number v. String)`

`77 does not strictly equal '77' because they have different types. However, if we were to test these values with loose equality…`

`77 == '77'`<br>
`// true` <br>

You can see we get `true`. That because of type coercion. JavaScript will actually try to convert our values into a like type. In this case, it succeeds. The string value of `'77'` can easily be converted into the number value of `77`. Since `77` equals `77`, we get our answer of `true`.

Lets look at one more example.

Recall earlier when we tested with strict equality if `false` equals `0`:
`false === 0`<br>
`// false (Different type and different value)`<br>

This is obviously false. However, if we run the same equation with loose equality…

`false == 0`<br>
`// true`<br>

We get `true`? Why is this? It has to do with **falsy** values in JavaScript.




