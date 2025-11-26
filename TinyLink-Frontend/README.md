# 🔗 TinyLink – URL Shortener (Spring Boot + React)

A clean, production-ready URL Shortener built using **Spring Boot** (Backend) and **React** (Frontend). Deployed on **Railway** (Backend + MySQL DB) and **Vercel** (Frontend). 🚀

---

## 🌍 Live Demo

🔗 **Frontend Live URL:** [https://tiny-link-aniket.vercel.app](https://tiny-link-aniket.vercel.app)

---

## 📂 GitHub Repositories

* **FullStack Repo:** [https://github.com/aniket-soni03/TinyLink.git](https://github.com/aniket-soni03/TinyLink.git)

---

## 🖥️ Backend — Spring Boot (Folder Structure)

```
src/main/java/com/url_shortner/
│
├── controller/
│   ├── LinkController.java
│   ├── RedirectController.java
│   └── HealthController.java
│
├── service/
│   ├── LinkService.java
│   └── RedirectService.java
│
├── dao/
│   └── LinkDao.java
│
├── repository/
│   └── LinkRepo.java
│
├── dto/
│   ├── LinkRequestDto.java
│   ├── LinkResponseDto.java
│   └── StatsResponseDto.java
│
├── exception/
│   ├── CodeAlreadyExistsException.java
│   ├── LinkNotFoundException.java
│   ├── InvalidUrlException.java
│   └── GlobalExceptionHandler.java
│
├── entity/
│   └── Link.java
│
├── config/
│   └── CorsConfig.java
│
└── TinyLinkApplication.java
```

---

## 🎨 Frontend — React (Folder Structure)

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

## 🛠️ Tech Stack

**Backend:**

* Spring Boot (REST API)
* **MySQL (Railway)**
* Spring Data JPA + Hibernate
* Custom Exception Handling
* CORS Config to allow Vercel

**Frontend:**

* React
* Custom CSS
* React Router
* Responsive UI

---

## 🔥 Core Features

* Create short URLs (with optional custom code)
* 302 redirect (`/:code`)
* Click tracking (total + last clicked)
* Delete links
* Dashboard `/`
* Stats page `/code/:code`
* Health check `/healthz`

---

## 📌 Environment Variables

### Backend — `application.properties`

```properties
spring.application.name=TinyLink-Backend

spring.datasource.url=${DB_URL}
spring.datasource.username=${DB_USERNAME}
spring.datasource.password=${DB_PASSWORD}
server.port=${PORT:8080}

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

### Railway Environment Variables

* `DB_URL` — MySQL JDBC URL
* `DB_USERNAME`
* `DB_PASSWORD`
* `SPRING_PROFILES_ACTIVE` - deploy  (MUST NEED TO CREATE)

---

## 🧾 API Endpoints

* **POST** `/api/links` — Create link
* **GET** `/api/links` — List all
* **GET** `/api/links/:code` — Stats for code
* **DELETE** `/api/links/:code` — Delete
* **GET** `/:code` — Redirect (302)
* **GET** `/healthz` — Health check

---

## 🚀 Deployment Notes

### Backend (Railway)

* Create a **MySQL database** inside Railway
* Copy credentials into ENV vars
* Deploy via GitHub → Railway auto-deploy

### Frontend (Vercel)

* Connect GitHub → Auto deploy
* Add ENV var `VITE_API_BASE_URL`

---

## 💙 Author

Made with ❤️ by **Aniket Soni**
