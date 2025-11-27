# 🚀 TinyLink Backend

A high-performance URL-shortening backend built with **Spring Boot**, connected to **MySQL**, and deployed on **Railway**.

---

## 🛠️ Tech Stack

* **Java 17**
* **Spring Boot 3.x**
* **MySQL (Railway)**
* **JPA / Hibernate**
* **Maven**

---

## 📁 Project Structure

```
src/main/java/com/url_shortner
│── controller
│── service
│── repository
│── model
│── dto
│── config
```

---

## 🔗 API Endpoints

### 1️⃣ Create Short URL

`POST /api/url`

### 2️⃣ Redirect to Original URL

`GET /{code}`

### 3️⃣ Health Check

`GET /health`

---

## ⚙️ Environment Variables

Create these in **Railway → Variables**:

| Variable                 | Description                      |
| ------------------------ | -------------------------------- |
| `DB_URL`                 | MySQL JDBC URL                   |
| `DB_USERNAME`            | Railway DB username              |
| `DB_PASSWORD`            | Railway DB password              |
| `SPRING_PROFILES_ACTIVE` | **deploy** (MUST NEED TO CREATE) |

⚠️ **Important Note:**
I have used **two application properties files**:

1. `application.properties` → Contains all **local** configurations
2. `application-deploy.properties` → Contains **Railway MySQL** configurations

👉 You **must switch profile** using:

```
SPRING_PROFILES_ACTIVE=deploy
```

Otherwise, your backend will use local MySQL and will **NOT connect to Railway**.

---

## 🗄️ Database

This project uses **MySQL on Railway**.
A `url_data` table is auto-created by JPA.

---

## 🚀 Deployment (Railway)

### 1️⃣ Push your backend project to GitHub

### 2️⃣ Create a new Railway project

### 3️⃣ Select "Deploy from GitHub Repository"

### 4️⃣ Add MySQL plugin inside Railway

### 5️⃣ Add Environment Variables (mentioned above)

### 6️⃣ Deploy → Railway builds and starts the JAR automatically

---

## ▶️ Run Locally

```
mvn clean install
mvn spring-boot:run
```

Or:

```
java -jar target/tinylink-1.0.jar
```

---

## 🤝 Contributing

Pull requests are welcome!

---

## 📬 Contact

For queries or issues, feel free to reach out.
