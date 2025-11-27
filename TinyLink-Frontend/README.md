<<<<<<< HEAD
# 🎨 TinyLink Frontend – React

A clean and responsive **React** frontend for the TinyLink URL Shortener project. Fully optimized and deployed on **Vercel**. 🚀
=======
# TinyLink Frontend

A clean and responsive React-based frontend for generating and managing short URLs with real-time validations, copy-to-clipboard, toast notifications, and a modern UI.
>>>>>>> a044e50 (properties file updated)

---

## 🚀 Live Demo

🔗 **Live URL:** `https://tiny-link-aniket.vercel.app`

---

<<<<<<< HEAD
## 📂 Folder Structure
=======
---

## 🛠️ Tech Stack

* **React.js** (Vite or CRA)
* **Fetch** for API communication
* **React-Toastify** for notifications
* **CSS Modules / Global CSS** for styling
* **Deployed on Vercel**

---

## ✨ Features

* Simple and attractive UI
* URL validation
* Copy short URL with one click
* Beautiful modal UI
* Toast alerts for success & errors
* Fully responsive design
* Integrated with backend API

---

## 📁 Project Structure
>>>>>>> a044e50 (properties file updated)

```
src/
│
├── assets/                  # Images, icons, logos
│   ├── logo.png
│   └── copy-icon.svg
│
├── styles/                  # CSS for each component/page
│   ├── App.css
│   ├── Dashboard.css
│   ├── Stats.css
│   ├── AddLinkForm.css
│   ├── LinkTable.css
│   └── Modal.css
│
├── routes/                  # React Router setup
│   └── MyRoutes.jsx
│
├── components/              # Reusable components
│   ├── Header.jsx
│   ├── Footer.jsx
│   ├── AddLinkForm.jsx
│   ├── LinkTable.jsx
│   ├── Modal.jsx
│   └── CopyButton.jsx
│
├── pages/                   # Main pages
│   ├── Dashboard.jsx
│   ├── Stats.jsx
│   └── NotFound.jsx
│
├── App.jsx                  # Main App container
├── main.jsx                 # ReactDOM render
└── index.css                # Global styles

---

## ⚙️ Setup Instructions

### 1️⃣ Clone the Project

```bash
git clone <your-frontend-repo-url>
cd project-folder
```

### 2️⃣ Install Dependencies

```bash
npm install
```

### 4️⃣ Start Development Server

```bash
npm run dev
```

---

<<<<<<< HEAD
## 🌟 Features

* Beautiful and responsive UI
* Add new short links with validation
* Copy-to-clipboard functionality
* View full link table with search & filter
* Stats page with total clicks and last clicked time
* 404 handling & clean routing
* Smooth UX with modal interactions

---

## 🛠️ Tech Stack

* **React**
* **React Router**
* **Custom CSS** for styling
* **Fetch API / Axios** for backend communication
* **Vercel** for hosting

---

## 🔧 Environment Variables (Vercel)

Add this in Vercel → Project Settings → Environment Variables:

```
VITE_API_BASE_URL=https://your-backend-railway-url
```

This is used for all API calls such as:

* `/api/links`
* `/api/links/:code`
* `/code/:code`

---

## 🧠 Pages Overview

### `/` — Dashboard

* Add new short links
* View table of all links
* Delete links

### `/code/:code` — Stats Page

* Shows click count
* Shows last clicked time
* Shows full target URL

### `*` — NotFound Page

* Handles invalid URLs

---

## 🚀 Deploying to Vercel

1. Push your frontend code to GitHub
2. Go to **Vercel → New Project**
3. Select the GitHub repo
```

5. Deploy → Vercel gives a Live URL

---

## 🧾 API Communication

Frontend interacts with the backend:

* `POST /api/links` — Create link
* `GET /api/links` — Get all links
* `GET /api/links/:code` — Get stats
* `DELETE /api/links/:code` — Delete


---

## 📦 GitHub Repository

* **FullStack Repo:** [https://github.com/aniket-soni03/TinyLink.git](https://github.com/aniket-soni03/TinyLink.git)

---

## 💙 Author

Made with ❤️ by **Aniket Soni**
=======
## 🚀 Deployment (Vercel)

1. Push your project to GitHub
2. Go to **Vercel → New Project**
3. Import GitHub repo
4. Select **Framework: React**
5. Set **Environment Variable** (if needed) e.g. `VITE_BACKEND_URL`
6. Deploy

---

## 🔗 API Endpoints Used

* `POST /create` – Create short URL
* `GET /{code}` – Redirect to original URL
* `GET /health` – Check server status

---

---

## 🙌 Author

**Aniket Soni**

>>>>>>> a044e50 (properties file updated)
