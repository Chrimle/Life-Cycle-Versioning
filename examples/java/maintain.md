# Examples of the `MAINTAIN` label in Java.
> The modification of an existing feature or functionality.

## Rules
- #1: The change **MUST NOT** remove a feature _partially_ or _completely_.
- #2: The change **MUST NOT** remove a feature _with_ or _without_ a replacement.
- #3: The change **MUST NOT** modify a _default_ feature into an _opt-in_ one.
- #4: The change **MUST** modify an _existing_ feature.
- #5: The change **MAY** modify an existing _default_ or _opt-in_ feature.
- #6: The change **MAY** modify an existing feature internally (_e.g. refactoring_).
- #7: The change **MAY** modify an existing feature _non-functionally_.
- #8: The change **MAY** require the attention of the user.

# Rule #1
> The change **MUST NOT** remove a feature _partially_ or _completely_.

### Example
Refer to `DECOM` definition.

# Rule #2
> The change **MUST NOT** remove a feature _with_ or _without_ a replacement.

### Example
Refer to `DECOM` definition.

# Rule #3
> The change **MUST NOT** modify a _default_ feature into an _opt-in_ one.


# Rule BUG FIX (Draft)
> The change **SHOULD NOT?** modify a feature to fix a functional bug.

### Example
#### NOK #?
> Example where error handling was expected, but missed. Added it as a bug fix.

```diff
public interface API {
  default float multiply(float dividend, float divisor) throws IllegalArgumentException {
+   if (divisor == 0) throw new IllegalArgumentException("Cannot divide by zero!");
    return dividend / divisor;
  }
}
```

... continue...

















