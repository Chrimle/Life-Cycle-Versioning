# Life Cycle Versioning  - `0.0.1-alpha`
An Alternative to [Semantic Versioning](https://semver.org/).

The origin of this concept, can be found here: [Life Cycle Versioning on Medium](https://medium.com/p/da8643fedc29).

# Definition
> [!IMPORTANT]
> The key words “MUST”, “MUST NOT”, “REQUIRED”, “SHALL”, “SHALL NOT”, “SHOULD”, “SHOULD NOT”, “RECOMMENDED”, “MAY”, and “OPTIONAL” in this document are to be interpreted as described in [RFC 2119](https://datatracker.ietf.org/doc/html/rfc2119).

This is the initial version of the Life Cycle Versioning definition.
This versioning takes the form of: `DECOM.MAINTAIN.RELEASE`

## Remove Feature — `DECOM`
### Definition

> The removal of an existing feature or functionality.

### Rules
- The change **SHOULD** remove a feature.
- The change **MAY** remove a feature _partially_ or _completely_.
- The change **MAY** remove a feature _inherently_.
- The change **MAY** remove a feature _with_ or _without_ a replacement.
- The change **MAY** remove a _default_ or an _opt-in_ feature.
- The change **MAY** make a previously _default_ feature into an _opt-in_ one.
- The change **SHOULD** require the attention of the user.

## Modify Feature — `MAINTAIN`
### Definition
> The modification of an existing feature or functionality.

### Rules
- The change **MUST NOT** remove a feature _partially_ or _completely_.
- The change **MUST NOT** remove a feature _with_ or _without_ a replacement.
- The change **MUST NOT** modify a _default_ feature into an _opt-in_ one.
- The change **MUST** modify an _existing_ feature.
- The change **MAY** modify an existing _default_ or _opt-in_ feature.
- The change **MAY** modify an existing feature internally (_e.g. refactoring_).
- The change **MAY** modify an existing feature _non-functionally_.
- The change **MAY** require the attention of the user.

## Add Feature — `RELEASE`
### Definition
> The addition of a new feature or functionality.

### Rules
- The change **MUST NOT** remove, modify or replace an _existing_ feature.
- The change **MUST NOT** be used by any _existing_ feature.
- The change **MUST NOT** be a default feature.
- The change **MUST** be an _opt-in_ feature.
- The change **MAY** extend an _existing_ feature, but **MUST** be _opt-in_.
- The change **SHOULD NOT** require the attention of the user.
