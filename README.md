Here’s a polished **README.md** you can use for your GitHub profile. It explains your Go project clearly, shows example outputs, and looks professional.

---

# 📚 Book Management API (Go + Gin)

This is a simple **RESTful API** built with [Go](https://golang.org/) and the [Gin web framework](https://github.com/gin-gonic/gin).
The API allows you to manage a small library of books with features such as:

* 📖 Get all books
* 🔎 Get a book by ID
* ➕ Add a new book
* ✅ Checkout a book (decrease quantity)
* 🔄 Return a book (increase quantity)

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/your-username/book-management-api.git
cd book-management-api
```

### 2. Install dependencies

Make sure you have Go installed (v1.18+ recommended).
Then install Gin:

```bash
go get -u github.com/gin-gonic/gin
```

### 3. Run the server

```bash
go run main.go
```

The server will start on:

```
http://localhost:8080
```

---

## 📌 API Endpoints

### 1. Get all books

**Request**

```bash
GET /books
```

**Response**

```json
[
  {
    "id": "1",
    "title": "In search of Lost Time",
    "author": "Marcel Proust",
    "quantity": 2
  },
  {
    "id": "2",
    "title": "The Great Gatsby",
    "author": "F. Scott Fitzgerald",
    "quantity": 5
  },
  {
    "id": "3",
    "title": "War and Peace",
    "author": "Leo Tolstoy",
    "quantity": 6
  }
]
```

---

### 2. Get a book by ID

**Request**

```bash
GET /books/2
```

**Response**

```json
{
  "id": "2",
  "title": "The Great Gatsby",
  "author": "F. Scott Fitzgerald",
  "quantity": 5
}
```

---

### 3. Add a new book

**Request**

```bash
POST /books
Content-Type: application/json

{
  "id": "4",
  "title": "1984",
  "author": "George Orwell",
  "quantity": 3
}
```

**Response**

```json
{
  "id": "4",
  "title": "1984",
  "author": "George Orwell",
  "quantity": 3
}
```

---

### 4. Checkout a book

**Request**

```bash
PATCH /checkout?id=2
```

**Response**

```json
{
  "id": "2",
  "title": "The Great Gatsby",
  "author": "F. Scott Fitzgerald",
  "quantity": 4
}
```

---

### 5. Return a book

**Request**

```bash
PATCH /return?id=2
```

**Response**

```json
{
  "id": "2",
  "title": "The Great Gatsby",
  "author": "F. Scott Fitzgerald",
  "quantity": 5
}
```

---

## 🛠 Features

* RESTful API with Gin
* JSON-based responses
* In-memory storage (no external DB required)
* Easy to extend (you can connect to a database later)

---

## 📷 Example Run (Terminal)

```bash
$ go run main.go
[GIN-debug] Listening and serving HTTP on localhost:8080
```

Then test using `curl`:

```bash
curl http://localhost:8080/books
```

---

## 🤝 Contributing

Feel free to fork this repo and open pull requests for improvements!

---

## 📄 License

Brian Mwenda Ndumba

---

<img width="1911" height="975" alt="image" src="https://github.com/user-attachments/assets/8fe57e68-47da-4e97-b6e2-91866a2a66a2" />

