# Unhandled FormatException during JSON Decoding in Dart

This repository demonstrates a common error in Dart applications: failing to handle `FormatException` exceptions that can occur when attempting to decode invalid JSON responses from an API.

The `bug.dart` file contains code that fetches data from an API and attempts to decode the response as JSON.  If the API returns data that is not valid JSON, a `FormatException` is thrown, causing the app to crash.  The solution addresses this issue by adding more robust error handling.

## How to reproduce

1. Clone this repository.
2. Run the `bug.dart` file.  (Ensure you have a Dart SDK installed)
3. Observe the crash, or if using a debugger, see the `FormatException`. 

## Solution

The `bugSolution.dart` file demonstrates a solution.  It wraps the `jsonDecode` call in a `try-catch` block to gracefully handle `FormatException`s, preventing the app from crashing.