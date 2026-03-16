# Technical Setup Guide - Radha Study Halls

To get this website fully functional for your specific needs, you will need to set up your own database and authentication services.

## 1. Firebase Setup (Authentication & Hosting)

The project uses Firebase for user authentication and hosting.

### Steps:
1. Go to [Firebase Console](https://console.firebase.google.com/).
2. Create a new project called **Radha Study Halls**.
3. Enable **Authentication** and choose **Email/Password** and **Google** (if needed).
4. Go to Project Settings and copy your **Firebase Config** (API Key, Auth Domain, Project ID, etc.).
5. Replace the configuration in `index.js`, `register.js`, and `checkin.js` with your new config.
6. Install Firebase CLI and run `firebase deploy` to host it.

## 2. MongoDB Setup (Database)

The project uses MongoDB to store student records and seat management data.

### Steps:
### Steps:
1. Create an account on [MongoDB Atlas](https://www.mongodb.com/cloud/atlas).
2. Create a new cluster and a database named **radha_study_halls**.
3. Create collections: `users`, `seats`, `enquiries`, `reviews`.
4. Get your **Connection String** from Atlas.
5. In your backend environment, use the following credentials:
   - **Username:** `goudadeepthi04_db_user`
   - **Password:** `OZKU8hxUSxhqdplB`
   - **Connection URL Template:** `mongodb+srv://goudadeepthi04_db_user:OZKU8hxUSxhqdplB@YOUR_CLUSTER_NAME.mongodb.net/radha_study_halls`

## 3. Backend Hosting (Railway)

The Enquiry form uses a separate backend API to process and store messages.

### Steps:
1. Create an account on [Railway.app](https://railway.app/).
2. Deploy your backend code (Node.js/Python) to a new service.
3. Get the **Generated Domain URL** (e.g., `https://your-backend.up.railway.app`).
4. Update `index.js` (Line 156) by replacing `YOUR_BACKEND_API_URL` with your Railway URL.

## 4. GitHub Integration

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
