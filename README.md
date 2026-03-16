
# 🛒 E-Commerce Microservices System

This project is a backend **E-Commerce system built using Spring Boot Microservices Architecture**.

The system is divided into independent services that communicate through **API Gateway and Service Discovery (Eureka)**.

---

# 🚀 Technologies Used

* Java 21
* Spring Boot
* Spring Cloud
* Eureka Service Discovery
* API Gateway
* Spring Data JPA
* MySQL
* Maven
* REST APIs

---

# 🧩 Microservices

| Service          | Description                         |
| ---------------- | ----------------------------------- |
| service-registry | Eureka server for service discovery |
| api-gateway      | Entry point for all API requests    |
| user-service     | Handles user management             |
| product-service  | Manages product catalog             |
| order-service    | Handles order processing            |

---

# 🏗 Architecture

Client requests pass through the **API Gateway**, which routes requests to appropriate microservices.

Each microservice has its **own database**.

```
Client
   │
   ▼
API Gateway
   │
   ▼
 ┌───────────────┬───────────────┬───────────────┐
 │               │               │
User Service   Product Service   Order Service
 │               │               │
MySQL           MySQL           MySQL
        │
        ▼
   Eureka Server
```

---

# ⚙️ How to Run the Project

Start services in this order:

1️⃣ service-registry
2️⃣ user-service
3️⃣ product-service
4️⃣ order-service
5️⃣ api-gateway

Open Eureka dashboard:

http://localhost:8761

---

# 📬 API Examples

Create User

POST /users

```
{
"name": "Ajay",
"email": "ajay@test.com"
}
```

Create Product

POST /products

```
{
"name": "Laptop",
"price": 80000
}
```

Create Order

POST /orders

```
{
"userId": 1,
"productId": 1
}
```

#🚀 Project Services
Service	Description	Port
Service Registry	Eureka Service Discovery	8761
API Gateway	Central API entry point	8080
Product Service	Manages product catalog	8081
Order Service	Handles order processing	8082
User Service	Manages users	8083
▶️ How to Run the Project
Step 1 – Start Service Registry

Run:

ServiceRegistryApplication

Open Eureka Dashboard:

http://localhost:8761
Step 2 – Start Product Service

Run:

ProductServiceApplication

Test API:

http://localhost:8081/products
Step 3 – Start Order Service

Run:

OrderServiceApplication

Test API:

http://localhost:8082/orders
Step 4 – Start User Service

Run:

UserServiceApplication

Test API:

http://localhost:8083/users
Step 5 – Start API Gateway

Run:

ApiGatewayApplication

Now access APIs through the gateway.

🌐 Gateway API Calls

Get Products

http://localhost:8080/products

Get Orders

http://localhost:8080/orders

Get Users

http://localhost:8080/users


---

# 🎯 Learning Outcomes

* Microservices architecture
* Service discovery with Eureka
* API Gateway routing
* REST API design
* Database per service pattern
* Spring Boot development

---

# 👨‍💻 Author

Ajay Pratap
Java Full Stack Developer
