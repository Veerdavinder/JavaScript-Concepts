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

## Falsy Values

Okay,so why does `false == 0` in JavaScript. It's complex, but it's because in JavaScript `0` is a **falsy** value.

Type coercion will actually our zero into a false boolean, then `false` is equal to `false`.

There are only **six falsy values** in JavaScript you should be aware of:

1. `false` -- boolean false <br>
2. `0` -- number zero<br>
3. `""`-- empty string<br>
4. `null`<br>
5. `undefined`<br>
6. `NaN` -- Not A Number<br>

## Falsy Value Comparison

The following you can consider to be ‘rules’ of falsy values. These are things you should ultimately memorize if you will be working with JavaScript often.

1. `false`, `0`, and `""`

When comparing any of our first three falsy values with loose equality, they will always be equal! That’s because these values will all coerce into a `false` boolean.

`false == 0`<br>
`// true`<br>

`0 == ""`<br>
`// true`<br>

`"" == false`<br>
`// true`<br>

2. `null` and `undefined`

When comparing `null` and `undefined`, they are only equal to themselves and each other:

`null == null`<br>
`// true`<br>

`undefined == undefined`<br>
`// true`<br>


`null == undefined`<br>
`// true`<br>

If you try to compare `null` to any other value, it will return `false`.

3. `NaN`

Lastly, `NaN` is not equivalent to anything. Even cooler, it’s not even itself!

`NaN == null`<br>
`// false`<br>

`NaN == undefined`<br>
`// false`<br>

`NaN == NaN`<br>
`// false`<br>