# User Management API

## Description

User Management API adalah REST API sederhana yang digunakan untuk melakukan operasi **CRUD (Create, Read, Update, Delete)** terhadap data user.

API ini memungkinkan pengguna untuk:

* Menambahkan user baru
* Melihat data user
* Memperbarui data user
* Menghapus data user

Project ini dibuat menggunakan **Spring Boot** dengan arsitektur layered yang terdiri dari:

* Controller
* Service
* Repository
* DTO
* Entity
* Mapper

---

# Technologies Used

* Java
* Spring Boot
* Maven
* REST API
* JSON

---

# Base URL

```
http://localhost:8080
```

---

# Application Interface

Berikut tampilan antarmuka aplikasi web yang digunakan untuk mengelola data pengguna.

<img width="1919" height="907" alt="image" src="https://github.com/user-attachments/assets/ed946e55-f6c0-4799-b721-5f0daf032525" />


---

# API Endpoints

Berikut daftar endpoint yang tersedia pada API ini.

| Method | Endpoint        | Description     |
| ------ | --------------- | --------------- |
| POST   | /api/users      | Create new user |
| GET    | /api/users      | Get user data   |
| PUT    | /api/users/{id} | Update user     |
| DELETE | /api/users/{id} | Delete user     |

---

# 1. Create User

Endpoint ini digunakan untuk menambahkan data user baru.

## Endpoint

```
POST /api/users
```

## Request Body

```json
{
  "nama": "Halim",
  "usia": 21
}
```

## Response Success

```json
{
  "data": {
    "id": "random string",
    "nama": "Halim",
    "usia": 21
  }
}
```

## Response Failed

```json
{
  "error": "Invalid input data"
}
```

## Screenshot

<img width="1436" height="927" alt="Screenshot 2026-03-08 142722" src="https://github.com/user-attachments/assets/a0b8cd5c-2741-4efb-bcf2-a0c18989694b" />


<img width="1435" height="903" alt="Screenshot 2026-03-08 142746" src="https://github.com/user-attachments/assets/7ff2e972-3937-4ff9-8fe9-34cf868e4bfd" />


---

# 2. Get User

Endpoint ini digunakan untuk mengambil data user.

## Endpoint

```
GET /api/users
```

## Response Success

```json
{
  "data": {
    "id": "random string",
    "nama": "Halim",
    "usia": 21
  }
}
```

## Response Failed

```json
{
  "error": "User not found"
}
```

## Screenshot

<img width="1436" height="930" alt="image" src="https://github.com/user-attachments/assets/631f251f-8e07-4279-b26c-e3fccab03e8c" />


<img width="1437" height="928" alt="image" src="https://github.com/user-attachments/assets/3f0a1353-2b64-42f4-ab2e-81ea3447c420" />


---

# 3. Update User

Endpoint ini digunakan untuk memperbarui data user berdasarkan ID.

## Endpoint

```
PUT /api/users/{id}
```

## Request Body

```json
{
  "nama": "Halim Update",
  "usia": 21
}
```

## Response Success

```json
{
  "data": {
    "id": "random string",
    "nama": "Halim Update",
    "usia": 21
  }
}
```

## Response Failed

```json
{
  "error": "User not found"
}
```

## Screenshot

<img width="1437" height="928" alt="image" src="https://github.com/user-attachments/assets/1717813a-f768-4448-a55d-ef7d3d8ea7e6" />


<img width="1436" height="929" alt="image" src="https://github.com/user-attachments/assets/45d0f3f5-b0f0-41b9-ae00-d38389223836" />


---

# 4. Delete User

Endpoint ini digunakan untuk menghapus data user berdasarkan ID.

## Endpoint

```
DELETE /api/users/{id}
```

## Response Success

```json
{
  "message": "User deleted successfully"
}
```

## Response Failed

```json
{
  "error": "User not found"
}
```

## Screenshot

<img width="1434" height="929" alt="image" src="https://github.com/user-attachments/assets/79423008-f37e-4608-a3d6-a8ae6255c948" />


<img width="1437" height="929" alt="image" src="https://github.com/user-attachments/assets/bd770082-a09f-49b0-9653-c3e2b97f61ed" />


---

# Project Structure

Berikut struktur utama project:

```
src
 └── main
     └── java
         └── com.deploy.praktikum1
             ├── controller
             ├── service
             ├── repository
             ├── entity
             ├── dto
             ├── mapper
             └── util
```

Arsitektur ini menggunakan **Layered Architecture** untuk memisahkan tanggung jawab tiap bagian aplikasi.

---
