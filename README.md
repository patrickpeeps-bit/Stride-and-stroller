# 🏃‍♀️ Stride & Stroller Community App

A robust, real-time, and geographically aware **Progressive Web App (PWA)** designed to help parents and caregivers organize local walking and stroller groups. It functions as a complete community platform, offering event creation, RSVP management, and geographical discovery.

The entire application is built into a **single HTML file** for deployment simplicity, using vanilla JavaScript, Tailwind CSS, and powered by Firebase.

---

## 🌟 Key Features

* **Real-Time Collaboration:** All walk listings, RSVPs (including guest and child counts), and host announcements update instantly across all users.
* **Host Management:** Event creators can safely edit, cancel (with history preserved), and manage their walk details.
* **Geographical Discovery:** Users can filter and sort walks by **distance** (5, 10, 25 miles) from their current location.
* **Advanced Filtering & Sorting:** Search by title/location and sort results by **Time** (default), **Distance**, or **Popularity** (total attendees).
* **Persistent Profiles:** Users set a display name and save their preferred **Time Zone**, ensuring accurate display of event times regardless of their travel location.
* **PWA Ready:** Includes a `manifest.json` for seamless installation to mobile home screens.

## 🛠 Technology Stack

* **Frontend:** HTML5, Vanilla JavaScript (ES6+), **Tailwind CSS** (via CDN)
* **Mapping:** **Leaflet.js** (for interactive maps and location search)
* **Backend/Database:** Google **Firebase** (Firestore for data, Auth for user management)
* **Deployment:** Firebase Hosting

---

## 🚀 Getting Started

To get this app running on your own server, follow these steps:

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/](https://github.com/)[YourUsername]/stride-stroller-community-app.git
    cd stride-stroller-community-app
    ```
2.  **Initialize Firebase Project:**
    * Create a new project in the **Firebase Console** (we recommend using the ID `stride-stroller-app`).
    * Install the Firebase CLI globally: `npm install -g firebase-tools`
    * Log in and initialize the project: `firebase login` and then `firebase init` (select Hosting, use the `public` directory, and configure as a single-page app).
3.  **Configure Firebase Credentials:**
    * You must provide the Firebase Config object (`firebaseConfig`) and the `initialAuthToken` (or use the Canvas environment variables) inside `public/index.html` if running outside of a secure environment.

4.  **Deployment:**
    * To deploy the app to your live URL:
        ```bash
        firebase deploy --only hosting
        ```

---

## ⚙️ Development Note

The core application logic is contained entirely within the self-contained file: `public/index.html`. All CSS, JavaScript, and HTML are merged into this single file for deployment simplicity.
