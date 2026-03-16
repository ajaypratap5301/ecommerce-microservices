# 🛒 E-Commerce Microservices System

A backend **E-Commerce system built using Spring Boot Microservices Architecture**.
The system is divided into independent services that communicate through **Eureka Service Discovery** and are accessed through an **API Gateway**.

This project demonstrates how to design and implement **scalable microservices with Spring Boot**.

---

# 🚀 Technologies Used

* Java 21
* Spring Boot
* Spring Cloud
* Eureka Server (Service Discovery)
* Spring Cloud Gateway
* Spring Data JPA
* MySQL
* Maven
* REST APIs

---

# 🧩 Microservices

| Service          | Description                         | Port |
| ---------------- | ----------------------------------- | ---- |
| service-registry | Eureka Server for service discovery | 8761 |
| api-gateway      | Central entry point for all APIs    | 8080 |
| product-service  | Manages product catalog             | 8081 |
| order-service    | Handles order processing            | 8082 |
| user-service     | Manages user information            | 8083 |

---

# 🏗 System Architecture

All client requests go through the **API Gateway**, which routes them to the appropriate microservice.
Each microservice has its **own database**, following the **Database-per-Service pattern**.

```
Client
   │
   ▼
API Gateway (8080)
   │
   ▼
 ┌───────────────┬───────────────┬───────────────┐
 │               │               │
User Service   Product Service   Order Service
(8083)         (8081)            (8082)
 │               │               │
MySQL           MySQL           MySQL
        │
        ▼
Eureka Server (8761)
```

---

# ▶️ How to Run the Project

Start the services in the following order.

### 1️⃣ Start Service Registry

Run:

```
ServiceRegistryApplication
```

Open Eureka Dashboard:

```
http://localhost:8761
```

---

### 2️⃣ Start Product Service

Run:

```
ProductServiceApplication
```

Test API:

```
http://localhost:8081/products
```

---

### 3️⃣ Start Order Service

Run:

```
OrderServiceApplication
```

Test API:

```
http://localhost:8082/orders
```

---

### 4️⃣ Start User Service

Run:

```
UserServiceApplication
```

Test API:

```
http://localhost:8083/users
```

---

### 5️⃣ Start API Gateway

Run:

```
ApiGatewayApplication
```

Now access APIs through the **API Gateway**.

---

# 🌐 API Gateway Endpoints

Access services through the gateway:

Get Products

```
GET http://localhost:8080/products
```

Get Orders

```
GET http://localhost:8080/orders
```

Get Users

```
GET http://localhost:8080/users
```

---

# 📬 Sample API Requests

### Create User

```
POST /users
```

Request Body

```
{
  "name": "Ajay",
  "email": "ajay@test.com"
}
```

---

### Create Product

```
POST /products
```

Request Body

```
{
  "name": "Laptop",
  "price": 80000
}
```

---

### Create Order

```
POST /orders
```

Request Body

```
{
  "userId": 1,
  "productId": 1
}
```

---

# 🎯 Learning Outcomes

Through this project you will understand:

* Microservices architecture with Spring Boot
* Service discovery using Eureka
* API Gateway routing
* REST API development
* Database per microservice pattern
* Building scalable backend systems

---

# 👨‍💻 Author

**Ajay Pratap**
Java Full Stack Developer
