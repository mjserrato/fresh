# Fresh 🍋

[![Pub](https://img.shields.io/pub/v/fresh.svg)](https://pub.dev/packages/fresh)
[![style: effective dart](https://img.shields.io/badge/style-effective_dart-40c4ff.svg)](https://github.com/tenhobi/effective_dart)
[![License: MIT](https://img.shields.io/badge/license-MIT-purple.svg)](https://opensource.org/licenses/MIT)

---

A [dio](https://pub.dev/packages/dio) interceptor for built-in token refresh.

## Overview

Fresh is a [dio](https://pub.dev/packages/dio) interceptor which attempts to simplify custom API authentication by integrating token refresh and caching transparently. Fresh is flexible and is intended to support custom token refresh mechanisms.

## Usage

```dart
dio.interceptors.add(
  Fresh<OAuth2Token>(
    tokenStorage: InMemoryTokenStorage(),
    refreshToken: (token, client) {
      // Perform refresh and return new token
    },
  ),
);
```

## Example

See [the example](https://github.com/felangel/fresh/tree/master/example) for a complete sample application using `fresh` which integrates with [jsonplaceholder](https://jsonplaceholder.typicode.com).
