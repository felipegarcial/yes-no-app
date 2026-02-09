# Yes No App

A Flutter chat application where you ask yes/no questions to a character named **Lana**, and she replies with a random answer and a GIF from the [yesno.wtf](https://yesno.wtf) API.

<img width="600" alt="image" src="https://github.com/user-attachments/assets/6c4cce22-ca91-4e32-8686-f6b2c28b65bd" />


## How It Works

1. Type a message ending with `?`
2. The app fetches a random yes/no answer + GIF from the API
3. Lana's reply appears in the chat with the animated GIF

## Architecture

Clean Architecture with Provider for state management:

```
lib/
├── main.dart
├── config/
│   ├── helpers/          # API helper (Dio + yesno.wtf)
│   └── theme/            # Material 3 theme (7 color options)
├── domain/
│   └── entities/         # Message entity
├── infraestructure/
│   └── models/           # YesNoModel (API response mapping)
└── presentation/
    ├── providers/        # ChatProvider (ChangeNotifier)
    ├── screens/          # ChatScreen
    └── widgets/          # Message bubbles, input field
```

## Tech Stack

- **Flutter** with Material 3
- **Provider** for state management
- **Dio** for HTTP requests
- **yesno.wtf** public API

## Getting Started

```bash
flutter pub get
flutter run
```
