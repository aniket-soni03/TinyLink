# 🎨 TinyLink Frontend – React

A clean and responsive **React** frontend for the TinyLink URL Shortener project. Fully optimized and deployed on **Vercel**. 🚀

---

## 🌍 Live Demo

🔗 **Frontend Live URL:** [https://tiny-link-aniket.vercel.app](https://tiny-link-aniket.vercel.app)

---

## 📂 Folder Structure

```
src/
│
├── assets/
│   ├── logo.png
│   └── copy-icon.svg
│
├── styles/
│   ├── App.css
│   ├── Dashboard.css
│   ├── Stats.css
│   ├── AddLinkForm.css
│   ├── LinkTable.css
│   └── Modal.css
│
├── routes/
│   └── MyRoutes.jsx
│
├── components/
│   ├── Header.jsx
│   ├── Footer.jsx
│   ├── AddLinkForm.jsx
│   ├── LinkTable.jsx
│   ├── Modal.jsx
│   └── CopyButton.jsx
│
├── pages/
│   ├── Dashboard.jsx
│   ├── Stats.jsx
│   └── NotFound.jsx
│
├── App.jsx
├── main.jsx
└── index.css
```

---

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
