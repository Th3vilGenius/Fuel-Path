# FuelPath — shareable web app (PWA)

This edition runs on iPhone and Android from a normal HTTPS website link. It supports profiles, personalized general wellness guidance, exercise suggestions, six cooking recipes, weight history, habit tracking, data export/deletion, and Add to Home Screen. It saves data **only in each user's own browser**.

## Get a public link with GitHub Pages

1. Sign in to GitHub and create a new **public** repository named `fuelpath`.
2. Upload the **contents of this folder** (index.html, app.js, manifest.webmanifest, icon.svg, sw.js) to the repository root. Do not upload the ZIP without extracting it.
3. In repository **Settings → Pages**, select **Deploy from a branch**, branch **main**, folder **/(root)**, and save.
4. Once GitHub Pages finishes deploying, your shareable URL will look like `https://YOUR-USERNAME.github.io/fuelpath/`. Replace YOUR-USERNAME with your actual GitHub username. This is an example, not a live URL.
5. Share that URL. People can open it on iPhone or Android and use Add to Home Screen to install it as a web app.

GitHub Pages hosts static files only. This version has no account login, cross-device sync, backend, or cloud database. Anyone who can access the public URL can use the app, but **each user's personal data stays in their own browser**.

## Health sync and notifications — important limits

- This PWA **does not sync** with Apple Health, Samsung Health, or Android Health Connect. Browser apps cannot directly use those native APIs. The separate Expo native source project is a foundation for those integrations but requires additional native configuration, testing, signing, and distribution.
- The web app can request notification permission on compatible devices but **does not schedule background notifications**. Reliable scheduled reminders require a native app or push service with backend and user consent.
- iOS/Android app-store publication requires developer accounts, signing, review, privacy policies, and platform-specific setup. GitHub Pages does not create App Store or Play Store apps.

## Privacy and safety

This is an educational prototype, not a medical device. It does not prescribe calorie deficits or extended fasting. It gives conservative guidance and flags users under 18 or with relevant health considerations for professional advice. The profile and weight data are stored in browser localStorage and can be exported or deleted in Settings. Clearing browser data can erase them. There is no encrypted account storage or recovery. Before commercial launch, commission security/privacy/accessibility and clinical content reviews, add age-appropriate safeguards, allergy filters, a privacy policy, and proper native health permission handling.
