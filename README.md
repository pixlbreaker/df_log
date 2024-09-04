# Dart Package Template

<a href="https://www.buymeacoffee.com/robmllze" target="_blank"><img align="right" src="https://cdn.buymeacoffee.com/buttons/default-orange.png" alt="Buy Me A Coffee" height="41" width="174"></a>

Dart & Flutter Packages by DevCetra.com & contributors.

[![pub package](https://img.shields.io/pub/v/df_log.svg)](https://pub.dev/packages/df_log)
[![MIT License](https://img.shields.io/badge/License-MIT-blue.svg)](https://raw.githubusercontent.com/robmllze/df_log/main/LICENSE)

## Summary

A package that provides logging utilities for better debugging. This debugging package adds different types of debugging message types for all types of logging types. For a full feature set, please refer to the [API reference](https://pub.dev/documentation/df_log/).

## Introduction

### What is this project?

The Dart Package Template is a powerful utility that provides logging functionalities for Dart and Flutter applications. It simplifies the process of debugging by offering various logging methods, making it easier to track the flow of your application and identify potential issues.

### Who should use this package?

This package is ideal for Dart and Flutter developers who need a reliable and easy-to-use logging system. Whether you're building a simple app or a complex system, this package will help you maintain clarity in your debugging process.

## Getting Started

### Prerequisites

Before using the Dart Package Template, ensure you have the following installed:

- Dart SDK version 2.12.0 or higher
- Flutter SDK version 2.0.0 or higher (if you're using this in a Flutter project)

### Installation

To install this package, add it as a dependency in your `pubspec.yaml` file:

```yaml
dependencies:
  df_log: ^<latest_version>
```

Replace `<latest_version>` with the latest version of the package available on [pub.dev](https://pub.dev/packages/df_log).

After updating the `pubspec.yaml` file, run the following command to fetch the package:

```bash
flutter pub get
```

## Usage Example

### Basic Setup

After installing the package, you can start using it in your project. Here’s a basic example:

```dart
import 'package:df_log/df_log.dart';

void main() {
  Here().debugLog('This is a log!'); // Prints: "⚪️ [main] This is a log!"
}
```

This simple example demonstrates how to log a basic message using the package.

### Examples

```dart
void main() {
  Here().debugLog('This is a log!'); // prints: "⚪️ [main] This is a log!"
  Here().debugLogError(
    'This is an error log!',
  ); // prints: "🔴 [main] This is an error log!"
  Here().debugLogAlert(
    'This is an alert log!',
  ); // prints: "🟠 [main] This is an alert log!"
  Here().debugLogIgnore(
    'This is an ignore log!',
  ); // prints: "🟡 [main] This is an ignore log!"
  Here().debugLogInfo(
    'This is an info log!',
  ); // prints: "🟣 [main] This is an info log!"
  Here().debugLogStart(
    'This is a start log!',
  ); // prints: "🔵 [main] This is a start log!"
  Here().debugLogStop(
    'This is a stop log!',
  ); // prints: "⚫ [main] This is a stop log!"
  Here().debugLogSuccess(
    'This is a success log!',
  ); // prints: "🟢 [main] This is a success log!"

  printRed(someFunction()); // prints: "someFunction" in red
  printGreen(anotherFunction()); // prints: "48"
  printLightPurple('You can also print in other color!');
}

String? someFunction() {
  return Here().scope;
}

int? anotherFunction() {
  return Here().lineNumber; // this is line 48
}
```

### Detailed Feature Explanation

The Dart Package Template provides various logging methods to suit different needs:

- `debugLog(String message)`: Logs a general debug message.
- `debugLogError(String message)`: Logs an error message.
- `debugLogAlert(String message)`: Logs an alert message.
- `debugLogInfo(String message)`: Logs an informational message.
- `debugLogStart(String message)`: Logs the start of a process.
- `debugLogStop(String message)`: Logs the stop of a process.
- `debugLogSuccess(String message)`: Logs a success message.

Each of these methods is designed to make it easy to categorize and differentiate between different types of logs.

### Customization

You can customize the logging output to fit your needs. For example, you can adjust the format of the logs, change the colors, or even extend the functionality to suit specific requirements.

Example:

```dart
Here().debugLog('Custom format log!', format: '[Custom] {message}');
```

## Advanced Usage

### Custom Logging Functions

If you need more specific logging functionalities, you can extend the `Here` class or create your own logging functions by wrapping the provided methods.

Example:

```dart
class CustomLogger extends Here {
  void logCustomMessage(String message) {
    debugLog('Custom: $message');
  }
}
```

### Integration with Other Packages

The Dart Package Template can be easily integrated with other packages like error reporting or analytics tools. For example, you can combine it with Firebase Crashlytics to log errors both locally and remotely:

```dart
void logErrorWithCrashlytics(String message) {
  Here().debugLogError(message);
  FirebaseCrashlytics.instance.log(message);
}
```

## Troubleshooting

### Common Issues

- **Logs not appearing in the console:** Ensure that the logging functions are called in the correct context, and the Dart/Flutter environment is correctly set up.
- **Custom log format not applied:** Verify that the custom format string is correctly passed to the logging method.

### FAQ

- **How do I change the log level?**
  - Currently, this package doesn't support log levels, but you can filter logs by implementing conditional logging based on your needs.

- **Can I use this package with Flutter Web?**
  - Yes, the package is compatible with Flutter Web.


## Contributing and Discussions

This is an open-source project, and we warmly welcome contributions from everyone, regardless of experience level. Whether you're a seasoned developer or just starting out, contributing to this project is a fantastic way to learn, share your knowledge, and make a meaningful impact on the community.

### Ways you can contribute:

- **Join the discussions and ask questions:** Your curiosity can lead to valuable insights and improvements.
- **Buy me a coffee:** If you'd like to support the project financially, consider [buying me a coffee](https://www.buymeacoffee.com/robmllze). Your support helps cover the costs of development and keeps the project growing.
- **Share your ideas:** Every perspective matters, and your ideas can spark innovation.
- **Report bugs:** Help us identify and fix issues to make the project more robust.
- **Suggest improvements or new features:** Your ideas can help shape the future of the project.
- **Help clarify documentation:** Good documentation is key to accessibility. You can make it easier for others to get started by improving or expanding our documentation.
- **Write articles:** Share your knowledge by writing tutorials, guides, or blog posts about your experiences with the project. It's a great way to contribute and help others learn.

No matter how you choose to contribute, your involvement is greatly appreciated and valued!

---

### Join Reddit Discussions:

💬 https://www.reddit.com/r/df_log/

### Join GitHub Discussions:

💬 https://github.com/robmllze/df_log/discussions/

### Chief Maintainer:

📧 Email _Robert Mollentze_ at robmllze@gmail.com

### Dontations:

If you're enjoying this package and find it valuable, consider showing your appreciation with a small donation. Every bit helps in supporting future development. You can donate here:

https://www.buymeacoffee.com/robmllze

---

## License

This project is released under the MIT License. See [LICENSE](https://raw.githubusercontent.com/robmllze/df_log/main/LICENSE) for more information.
