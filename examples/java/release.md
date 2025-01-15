# Examples of the `RELEASE` label in Java.
> The addition of a new feature or functionality.

## Rules
- #1: The change **MUST NOT** remove, modify or replace an _existing_ feature.
- #2: The change **MUST NOT** be used by any _existing_ feature.
- #3: The change **MUST NOT** be a _default_ feature.
- #4: The change **MUST** be an _opt-in_ feature.
- #5: The change **MAY** extend an _existing_ feature, but **MUST** be _opt-in_.
- #6: The change **SHOULD NOT** require the attention of the user.

# Rule #1
> The change **MUST NOT** remove, modify or replace an _existing_ feature.

### Example
#### NOK #1
```diff
public interface API {
-  int multiply(int a, int b);
}
```
#### NOK #2
```diff
public interface API {
-  int multiply(int a, int b);
+  long multiply(long a, long b);
}
```
#### NOK #3
```diff
public interface API {
-  int multiply(int a, int b);
+  int multiply(int a, int b, int c);
}
```
# Rule #2
> The change **MUST NOT** be used by any _existing_ feature.

### Example
#### NOK #1
```diff
public interface API {
  default int multiply(int a, int b) {
+   return multiply(a, b, 1);
  }

+ int multiply(int a, int b, int c);
}
```
# Rule #3
> The change **MUST NOT** be a _default_ feature.

### Example
#### NOK #1
_Not Applicable_


# Rule #4
> The change **MUST** be an _opt-in_ feature.

### Example
#### NOK #1
_Not Applicable_

# Rule #5
> The change **MAY** extend an _existing_ feature, but **MUST** be _opt-in_.

### Example
#### OK #1
```diff
public interface API {
  int multiply(int a, int b);

+ default int multiply(int a, int b, int c) {
+   return multiply(a, multiply(b, c));
+ }
}
```
