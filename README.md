# Banking Application

A simple **Banking Application** built using **Spring Boot and MySQL**.  
The application provides RESTful APIs to perform core banking operations like **account creation, deposit, withdrawal, and account management**.

---

## API Testing (Postman)

You can test all APIs using Postman by sending requests to:
```
http://localhost:8080/api/accounts
```

---

## Features

- Create a new bank account
- View account details by ID
- View all accounts
- Deposit money into an account
- Withdraw money from an account
- Delete an account

---

## Tech Stack

- `Java`
- `Spring Boot`
- `Spring Web (REST API)`
- `Spring Data JPA`
- `Hibernate`
- `MySQL`
- `Maven`

---

## Folder Structure

```
banking-app/
├── src/main/java
│ └── net.sarvesh.bankingapp
│ ├── controller # REST Controllers
│ ├── service # Business Logic
│ ├── repository # Data Access Layer
│ ├── entity # JPA Entities
│ ├── dto # Data Transfer Objects
│ └── BankingAppApplication.java
│
├── src/main/resources
│ └── application.properties
│
├── pom.xml
```

---

## ⚙️ Setup Instructions (Mac / Linux / Windows)

1. **Clone the repository**
```
git clone https://github.com/your-username/banking-app.git
cd banking-app
```

---

2. **Create MySQL database**
```sql
CREATE DATABASE banking_app;
```

---

3. **Configure database**

Update application.properties:
```
spring.datasource.url=jdbc:mysql://localhost:3306/banking_app
spring.datasource.username=YOUR_USERNAME
spring.datasource.password=YOUR_PASSWORD

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

---

4. **Run the application**

---

5. **Access the application**
Base URL:
```
http://localhost:8080/api/accounts
```

---

## API Endpoints

### Account Routes

| Method | Endpoint                          | Description                  |
|--------|----------------------------------|------------------------------|
| POST   | /api/accounts                    | Create new account           |
| GET    | /api/accounts/{id}               | Get account by ID            |
| GET    | /api/accounts/all                | Get all accounts             |
| PUT    | /api/accounts/{id}/deposit       | Deposit money                |
| PUT    | /api/accounts/{id}/withdraw      | Withdraw money               |
| DELETE | /api/accounts/{id}               | Delete account               |

---

## Postman API Testing Guide

### 1. Create Account
- Method: `POST`
- URL: `http://localhost:8080/api/accounts`
- Body (raw JSON):
```json
{
  "name": "Sarvesh",
  "balance": 1000
}
```

### 2. Get Account by ID
- Method: `POST`
- URL: `http://localhost:8080/api/accounts/{id}`

### 3. Get All Accounts
- Method: `POST`
- URL: `http://localhost:8080/api/accounts/all`

### 4. Deposit Money
- Method: `PUT`
- URL: `http://localhost:8080/api/accounts/{id}/deposit`
- Body (raw JSON):
```json
{
  "amount": 500
}
```

### 5. Withdraw Money
- Method: `PUT`
- URL: `http://localhost:8080/api/accounts/{id}/withdraw`
- Body (raw JSON):
```json
{
  "amount": 200
}
```

### 6. Delete Account
- Method: `DELETE`
- URL: `http://localhost:8080/api/accounts/{id}`

---

## Example Workflow

- `1. Create an account`
- `2. Deposit money`
- `3. Withdraw money`
- `4. Fetch updated account details`
