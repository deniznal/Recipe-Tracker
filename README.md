# Recipe Tracker

An Android application for discovering recipes, exploring food categories, and keeping a personal collection of favourite meals.

Recipe data is retrieved from [TheMealDB](https://www.themealdb.com/), while Firebase Authentication and Cloud Firestore handle user accounts and saved favourites.

## Features

- **Browse recipes:** Explore recipes organized by food categories.
- **Search recipes:** Find recipes by name.
- **Recipe details:** View recipe information, ingredients, measurements, and cooking instructions.
- **Favourite recipes:** Save recipes to a personal favourites list and remove them when no longer needed.
- **User accounts:** Create an account, sign in, and log out.

## Tech Stack

| Technology | Purpose |
|---|---|
| Kotlin | Application development |
| Android SDK | Android application platform |
| Firebase Authentication | User registration and login |
| Cloud Firestore | Storing user favourites |
| TheMealDB API | Recipe and category data |
| OkHttp | HTTP requests |
| Kotlin Coroutines | Background operations |
| Android Jetpack Navigation | Screen navigation |
| ViewModel & LiveData | UI state management |
| Glide | Loading recipe images |
| RecyclerView | Displaying recipe and category lists |
| XML & Material Components | User interface |

## Architecture

The application follows a separation of responsibilities between UI components and application logic.

```text
app/src/main/java/com/example/recipeappstep1/
├── adapter/       # RecyclerView adapters
├── fragment/      # Application screens
├── model/         # Recipe, category, and ingredient models
├── network/       # TheMealDB API communication
└── viewmodel/     # UI state and application logic
```

- **Fragments** manage individual screens and user interactions.
- **ViewModels** handle data operations and expose UI state through LiveData.
- **CallApi** communicates with TheMealDB and parses recipe and category responses.
- **Firebase** provides authentication and stores each user's favourite recipe IDs.

## Getting Started

### Prerequisites

- Android Studio
- JDK 11 or compatible Android Studio JDK
- An Android device or emulator running Android 7.0 (API 24) or newer
- A Firebase project with Authentication and Cloud Firestore enabled

### Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/deniznal/Recipe-Tracker.git
   cd Recipe-Tracker
   ```

2. Open the project in Android Studio.

3. Configure Firebase:
   - Create or select a Firebase project.
   - Register an Android application with the package name `com.example.recipeappstep1`.
   - Enable Email/Password authentication.
   - Create a Cloud Firestore database.
   - Add your Firebase configuration file as `app/google-services.json`.

4. Sync the Gradle project.

5. Build and run the application on an emulator or connected Android device.

## External Services

- [TheMealDB](https://www.themealdb.com/) — Provides recipe, category, ingredient, and instruction data.
- [Firebase](https://firebase.google.com/) — Provides account authentication and cloud storage for favourite recipes.

## Contributors

- **Deniz Nal** — Network communication, navigation, and fragment logic.
- **Berre Delikara** — UI design, implementation, and RecyclerView adapters.
