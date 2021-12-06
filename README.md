# React Native with Expo

## Steps to create and run a new project

- npm install -g expo-cli
- expo init gift-track
- select "tabs (TypeScript)" to start with
  TypeScript and react-navigation already configured
- cd gift-track
- yarn ios
  - runs Metro server
  - opens Metro page in default web browser
  - opens app in iOS Simulator

In Simulator, press cmd-ctrl-z to open developer menu.
This includes menu items for the following:

- Reload
- Copy link to clipboard
- Go to Home
- Disable Fast Refresh
- Debug Remote JS
- Show Performance Monitor
- Show Element Inspector

## Initial Files

- App.tsx
- .expo : excluded from Git in .gitignore
  - packager-info.json
  - settings.json
- .expo-shared
  - assets.json
- assets
  - fonts
    - SpaceMono-Regular.ttf
- assets
  - images
    - \*.png
- components
  - EditScreenInfo.tsx
  - StyledText.tsx
  - Themed.tsx
- constants
  - Colors.ts
  - Layout.ts
- hooks
  - useCachedResources.ts
  - useColorScheme.ts
- navigation
  - index.tsx
  - LinkingConfiguration.ts
- screens
  - ModalScreen.tsx
  - NotFoundScreen.tsx
  - TabOneScreen.tsx
  - TabTwoScreen.tsx

## ESLint

ESLint is not installed or configured by default.

- `npm install -D eslint eslint-plugin-react eslint-plugin-react-native`
- Create the file `.eslintrc` (see contents in this project).
- Add the following npm script in `package.json`.

  ```json
  "lint": "eslint --ignore-path .gitignore .",
  ```

- To run, enter `npm run lint`.

## Prettier

Prettier is not installed or configured by default.

- `npm install -D prettier`
- Create the file `.prettierrc` (see contents in this project).
- Add the following npm script in `package.json`.

  ```json
  "format": "prettier --write '**/*.{js,ts,tsx}'",
  ```

- To run, enter `npm run format`.
