# Pass an Array or vararg parameter as vararg in Kotlin

Sometimes, you are developing a function which receives a **vararg** parameter
and you want to also pass the values to another function which also expects a
_vararg_ parameter. In order to pass your values as _vararg_ you have to use the
spread operator (**\***):

```
fun format(text: String, vararg args: Any): String {
    return text.format(*args)
}
```

The spread operator is also useful to convert an array to a _vararg_ argument.
Examples:

```
val message = "Hello %s, today is %s!".format(*arrayOf("Arturo", "Tuesday"))
```
