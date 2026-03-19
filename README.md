# 🍔 Food Delivery App

A **Spring Boot-based web application** designed to manage a complete food delivery ecosystem, including users, restaurants, food items, and order processing.

This project uses **Spring Data JPA** for backend persistence and **Thymeleaf** for the frontend UI.

---

## 🚀 Features

### 👤 User Management

* Create, view, and delete users

### 🏪 Restaurant Management

* Register restaurants
* Assign food items to restaurant menus

### 🍕 Food Item Catalog

* Manage global list of food items
* Validation for price handling

### 📦 Order System

* Place orders linking:

  * Users
  * Restaurants
  * Food items

### ⚠️ Data Validation

* Custom exception handling
* Prevents:

  * Negative prices
  * Invalid location formats

---

## 🛠️ Tech Stack

| Category   | Technology                  |
| ---------- | --------------------------- |
| Framework  | Spring Boot 3.5.0           |
| Language   | Java 23                     |
| Database   | PostgreSQL                  |
| ORM        | Spring Data JPA / Hibernate |
| Frontend   | Thymeleaf                   |
| Build Tool | Maven                       |

---

## 📂 Project Structure

```
com.example.fooddeliveryapp
│
├── model        → JPA Entities (User, Restaurant, FoodItem, Orders)
├── controller   → Handles HTTP requests
├── service      → Business logic layer
├── repository   → JPA Repositories
│
└── resources
    └── templates → Thymeleaf HTML UI
```

---

## ⚙️ Prerequisites

* Java 23 installed
* PostgreSQL installed and running
* Database created:

  ```
  app_db
  ```

---

## 🔧 Configuration

Update your `application.properties`:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/app_db
spring.datasource.username=your_username
spring.datasource.password=your_password
```

---

## ▶️ How to Run

### Clone the repository

```
git clone https://github.com/HarshaUndodi/food-delivery-app.git
```

### Navigate to project

```
cd food-delivery-app
```

### Run the application

#### Windows:

```
mvnw.cmd spring-boot:run
```

#### Linux/macOS:

```
./mvnw spring-boot:run
```

---

## 🌐 Application Endpoints

| Module      | URL            |
| ----------- | -------------- |
| Users       | `/users/`      |
| Restaurants | `/restaurant/` |
| Food Items  | `/fooditem/`   |
| Orders      | `/orders/`     |

---

## 🧠 Validation Logic

* **Price Rule**
  If price ≤ 0 → defaults to `100`

* **Location Rule**
  First letter automatically capitalized if invalid

---

## 📌 Future Improvements

* Add authentication & authorization (Spring Security)
* REST API support (for frontend apps)
* Payment integration
* Docker deployment

---

## 👨‍💻 Author

**Harshavardhana Undodi**

---

⭐ If you found this useful, consider giving it a star!
