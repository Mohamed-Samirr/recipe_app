# Recipe App

A Flutter recipe discovery app for browsing meals by category, searching for recipes, and keeping track of saved recipes and shopping items.

## Features

- Onboarding screen with a quick start flow
- Browse recipes by breakfast, lunch, dinner, and quick-meal categories
- Search recipes by keyword or search tag
- View recipe images, preparation time, ingredients, calories, and unit information
- Open the original recipe instructions
- Share recipe links
- Save and remove favorite recipes locally
- Manage a local shopping list with share and delete actions
- Responsive UI for Android, iOS, web, desktop, and other Flutter-supported platforms

## Tech Stack

- **Flutter/Dart** for the application UI and platform support
- **Edamam Recipe API** for recipe search and nutrition data
- **Hive** for local saved recipes and shopping-list storage
- `share_plus` for sharing recipe links
- `url_launcher` for opening original recipe pages
- `google_nav_bar` for bottom navigation

## Project Structure

```text
lib/
├── components/   Reusable UI components
├── constants/    API, sharing, navigation, and helper utilities
├── screens/      Application screens
└── main.dart     App entry point and Hive initialization
images/           Local food and category images
test/             Flutter widget tests
```

## Getting Started

### Prerequisites

- Flutter SDK 3.22 or later
- Dart SDK 3.4.4 or later
- An Edamam Recipe API application ID and key

### Install and run

```bash
flutter pub get
flutter run
```

To run on a specific device, first list available targets:

```bash
flutter devices
flutter run -d <device-id>
```

## API Configuration

Recipe searches use the Edamam Recipe API. Before sharing or deploying the app, move the Edamam application ID and API key out of source control and provide them through a secure configuration mechanism. The API request is currently defined in:

```text
lib/constants/constant_functions.dart
```

The app requests recipe results with an alcohol-free health filter and a calorie range of 591–722 calories.

## Testing

Run the Flutter test suite with:

```bash
flutter test
```

## License

No license has been specified for this project yet.
