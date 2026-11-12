# CICT Org Fair

**Live site:** https://Y-say.github.io/my-strapi-project/

> Replace the URL above after your first successful GitHub Pages deployment.

A Flutter web + Android app for the CICT Organization Fair at West Visayas State University.
Built as part of CC 206 Web Development — Unit 7 & 8 assignments.

## Setup

1. Copy `cms.example.json` to `cms.json` and fill in your CMS values:
   ```json
   {
     "CMS": "strapi",
     "CMS_URL": "https://your-project.strapiapp.com",
     "CMS_TOKEN": "your-read-only-token"
   }
   ```

2. Install dependencies:
   ```
   flutter pub get
   ```

3. Run locally:
   ```
   flutter run --dart-define-from-file=cms.json
   ```

4. Build for web:
   ```
   flutter build web --release --dart-define-from-file=cms.json
   ```

## CI/CD

- **CI** (`ci.yml`): runs `flutter analyze`, `flutter test`, and a web smoke build on every push and pull request.
- **CD** (`deploy.yml`): builds and deploys to GitHub Pages on every push to `main`.

## Android Release

Build the signed APK:
```
flutter build apk --release --dart-define-from-file=cms.json
```
Output: `build/app/outputs/flutter-apk/app-release.apk`
