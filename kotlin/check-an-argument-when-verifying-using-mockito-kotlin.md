# Check an argument when verifying using Mockito Kotlin

Usually, you need to capture an argument to check value when verifying a mock
with Mockito and you, probably, know that the needed code is not too easy to
write.

You can use [Mockito Kotlin](https://github.com/nhaarman/mockito-kotlin) to
simplify, **a lot**, the needed code to validate an argument:

```kotlin
verify(myMockInstance).method(argThat { it.id == MY_EXPECTED_ID_VALUE})
```

You can use `check` instead of `argThat` to check several assertions at the
same time:

```kotlin
verify(myMockInstance).method(check {
  assertThat(it.id, `is`(MY_EXPECTED_ID_VALUE))
  assertThat(it.name, `is`(MY_EXPECTED_NAME))
})
```
