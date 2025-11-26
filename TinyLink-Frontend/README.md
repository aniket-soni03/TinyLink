# TinyLink 🚀

A URL shortener web app similar to Bit.ly built with **React** (frontend) and **Spring Boot** (backend) with **MySQL** as the database. Users can shorten URLs, create custom codes, track click statistics, and manage links.

---

## 📦 Features

* **Create Short Links**: Generate short URLs from long URLs.
* **Custom Codes**: Optional custom short codes, globally unique.
* **Redirect**: Visiting `/code` performs a `302 redirect`.
* **Click Tracking**: Increment click count and update last clicked timestamp.
* **Delete Links**: Remove links, stopping future redirects (`404`).
* **Dashboard**: View all links with stats and actions.
* **Stats Page**: View details of a single link.
* **Health Check**: `/healthz` endpoint returns server status.
* **User Feedback**: Toast notifications using `react-toastify`.
* **Responsive UI**: Clean layout, animations, and friendly UX.

---

## 🛠 Tech Stack

* **Frontend**: React, React Router, react-hook-form, react-toastify
* **Backend**: Spring Boot, Spring Data JPA
* **Database**: MySQL
* **Styling**: Custom CSS + animations
* **Build & Dev Tools**: Vite, Maven

---

## 📁 Project Structure

```
src/
│
├── assets/           # Images and icons
├── styles/           # Individual CSS files per component/page
├── routes/           # React Router setup (MyRoutes.jsx)
├── components/       # Reusable components (Header, Footer, CopyButton, Modal, LinkTable, AddLinkForm)
├── pages/            # Dashboard, Stats, NotFound pages
├── services/         # API service logic merged in components
├── App.jsx
├── main.jsx
└── index.css
```

Backend Spring Boot structure:

```
src/main/java/com/url_shortner/
│
├── controller/       # LinkController, RedirectController, HealthController
├── service/          # LinkService, RedirectService
├── dao/              # LinkDao
├── repository/       # LinkRepository
├── dto/              # LinkRequestDto, LinkResponseDto, StatsResponseDto
├── exception/        # Custom exceptions & global handler
├── entity/           # Link entity
├── config/           # AppConfig
└── TinyLinkApplication.java
```

---

## 🏃‍♂️ Getting Started

### Prerequisites

* Node.js >= 18
* Java 17+
* Maven
* MySQL database

### Backend Setup

1. Clone the repo and navigate to backend:

   ```bash
   cd tinylink-backend
   ```
2. Update `application.properties` or `.env` with your MySQL credentials.
3. Build and run:

   ```bash
   mvn spring-boot:run
   ```

   Backend will run on `http://localhost:8080`

### Frontend Setup

1. Navigate to frontend folder:

   ```bash
   cd tinylink-frontend
   ```
2. Install dependencies:

   ```bash
   npm install
   ```
3. Run dev server:

   ```bash
   npm run dev
   ```

   Frontend will run on `http://localhost:5173`

### Build & Deploy

* Backend: `mvn clean package`
* Frontend: `npm run build`
* Deploy on Vercel / Railway / Render + MySQL or Postgres

---

## 📌 API Endpoints

| Method | Path               | Description                                        |
| ------ | ------------------ | -------------------------------------------------- |
| GET    | `/healthz`         | Returns server status `{ ok: true, version: 1.0 }` |
| POST   | `/api/links`       | Create a new link (409 if code exists)             |
| GET    | `/api/links`       | List all links                                     |
| GET    | `/api/links/:code` | Stats for one code                                 |
| DELETE | `/api/links/:code` | Delete link                                        |
| GET    | `/:code`           | Redirect to original URL (302 or 404)              |

---

## 🎨 Frontend Pages

* **Dashboard `/`**: Add new link, view all links, delete links.
* **Stats `/code/:code`**: View click count, last clicked timestamp, original URL.
* **Redirect `/:code`**: Redirects to original URL.
* **404**: Page not found

---

## ✨ UX & UI

* Clean, minimal design with responsive layout.
* Loading, empty, success, and error states.
* Modal popup when a short URL is generated with Copy & Close buttons.
* Toast notifications for user feedback.
* Animations for modal and table actions.

---

## ⚙️ Environment Variables

Create a `.env.example`:

```
REACT_APP_BASE_URL=http://localhost:8080
DB_URL=jdbc:mysql://localhost:3306/tinylink
DB_USER=root
DB_PASSWORD=yourpassword
```

---

## 📹 Demo

* [Demo Video Link](#) (replace with your video explaining the project)

---

## 📚 Notes

* All endpoints and field names strictly follow PDF spec for autograding.
* Custom codes are validated `[A-Za-z0-9]{6,8}`.
* Modal popup and toast notifications provide a polished UX.
* Fully responsive and animated design.

---

## 💡 Future Improvements

* User authentication & personal link management.
* Pagination for dashboard table.
* Optional search/filter by code or URL.
* Analytics dashboard with charts.

---

Made with ❤️ by **Your Name**
