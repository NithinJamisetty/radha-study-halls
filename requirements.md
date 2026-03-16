# Technical Setup Guide - Radha Study Halls

To get this website fully functional for your specific needs, you will need to set up your own database and authentication services.

## 1. Firebase Setup (Authentication & Firestore)

The project uses Firebase for user authentication, seat management, reviews, and enquiries.

### Steps:
1. Go to [Firebase Console](https://console.firebase.google.com/).
2. Create a new project called **Radha Study Halls**.
3. Enable **Authentication** and choose **Email/Password**.
4. Enable **Cloud Firestore** and create collections for `users`, `seats`, `enquiries`, and `reviews`.
5. Go to Project Settings and copy your **Firebase Config**.
6. Replace the configuration in `index.js`, `register.js`, and `checkin.js` with your new config.
7. Install Firebase CLI and run `firebase deploy` to host it.

> [!NOTE]
> All data management (Seats, Enquiries, Reviews) is now fully handled by Firebase. No external backend or MongoDB is required.

## 2. GitHub Integration

The code is optimized to be pushed to your own GitHub repository.

- **Current Repository:** [https://github.com/NithinJamisetty/radha-study-halls](https://github.com/NithinJamisetty/radha-study-halls)
- **Push Instructions:**
  ```bash
  git remote add origin https://github.com/NithinJamisetty/radha-study-halls.git
  git push -u origin main
  ```

## 4. Personalization

- Search for any remaining mentions of the previous name and update them in the settings.
- Replace any remaining images in `icons/` with your own branding if necessary.
