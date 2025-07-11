# 🌐 All About APIs: Complete Guide for Developers & Interviews

This document is a **comprehensive reference for APIs**, covering everything from HTTP basics to advanced API implementation and interview prep.

> 🔹 **Target Audience**: Developers with any experience level  
> 🔹 **Covers**: REST, SOAP, HTTP, CRUD, status codes, headers, authentication, Postman, best practices, and practical examples

---

## 📘 What is an API?

An **API (Application Programming Interface)** enables software systems to communicate with each other.

- Acts as a **bridge** between client and server.
- Defines **rules**, **methods**, and **data formats** for interaction.

### 🔁 Example

Client → API → Server → API → Client

### 🧪 Real-Life Analogy

A **waiter** in a restaurant is like an API:
- You (client) ask for food (data)
- Waiter (API) takes the request to the kitchen (server)
- Kitchen prepares the food, and the waiter returns it

---

## 🌍 Types of APIs

| Type             | Description                             | Examples                 |
|------------------|-----------------------------------------|--------------------------|
| **Web APIs**     | Accessible via HTTP/HTTPS               | REST, SOAP, GraphQL      |
| **Library APIs** | Interface to a software library         | Java SDK, NumPy in Python|
| **Hardware APIs**| Communicate with physical devices       | Camera, Bluetooth APIs   |
| **Internal APIs**| For internal system/service communication| Microservices            |
| **Public APIs**  | Open to external developers             | Twitter, GitHub APIs     |

---

## 🕸️ Web API Categories

### ✅ REST (Representational State Transfer)
- Stateless, scalable
- Uses HTTP methods (GET, POST, etc.)
- Supports JSON
- Widely adopted

### 🔵 SOAP (Simple Object Access Protocol)
- XML based
- Strict and standard-heavy
- More secure, used in banking, enterprise

### ⚛️ GraphQL
- Flexible data query language
- One endpoint for all queries
- Reduces over-fetching

---

## 🚀 HTTP Basics

| Concept        | Description                               |
|----------------|-------------------------------------------|
| HTTP           | Protocol for transferring data            |
| URL            | Unique resource locator                   |
| Client         | Sends request (Postman, browser)          |
| Server         | Responds with data                        |
| Method         | HTTP verb (GET, POST, PUT, DELETE)        |
| Header         | Meta-data (Auth, content-type, etc.)      |
| Body           | Payload data (JSON/XML)                   |
| Status Code    | Result of the request (200, 404, etc.)    |

---

## 📮 HTTP Methods

| Method   | Action  | Description                             |
|----------|---------|-----------------------------------------|
| GET      | Read    | Retrieve data from server               |
| POST     | Create  | Create new data on server               |
| PUT      | Update  | Replace entire resource                 |
| PATCH    | Update  | Modify part of a resource               |
| DELETE   | Delete  | Remove a resource                       |
| OPTIONS  | -       | Shows supported methods for resource    |
| HEAD     | -       | Like GET but returns headers only       |

---

## 🧾 HTTP Status Codes

### ✅ 1XX - Informational
- `100 Continue` – Continue with request
- `101 Switching Protocols` – Protocol upgrade
- `103 Early Hints` – Preloading

### ✅ 2XX - Success
- `200 OK` – Request succeeded
- `201 Created` – Resource created
- `202 Accepted` – Accepted but not completed
- `203 Non-Authoritative` – From third party/cache
- `204 No Content` – No response body
- `205 Reset Content` – Clear input view
- `206 Partial Content` – For range requests

### 🔁 3XX - Redirection
- `301 Moved Permanently`
- `302 Found (Temporary)`
- `304 Not Modified` – Cached version
- `307 Temporary Redirect`
- `308 Permanent Redirect`

### 🚫 4XX - Client Errors
- `400 Bad Request`
- `401 Unauthorized`
- `403 Forbidden`
- `404 Not Found`
- `405 Method Not Allowed`
- `409 Conflict`
- `422 Unprocessable Entity`
- `429 Too Many Requests`

### 🛑 5XX - Server Errors
- `500 Internal Server Error`
- `501 Not Implemented`
- `502 Bad Gateway`
- `503 Service Unavailable`
- `504 Gateway Timeout`

---

## 🧩 Request Components

### Headers

| Header          | Description                              |
|------------------|------------------------------------------|
| Content-Type     | Format of request/response body          |
| Authorization    | API keys, tokens                         |
| Accept           | Expected response format                 |
| Cache-Control    | Caching policy                           |
| User-Agent       | Info about client                        |

### Body

- Used in POST/PUT/PATCH
- Sent in JSON/XML format
- Represents actual data

---

## 🛡️ API Authentication

| Method          | Description                             |
|------------------|-----------------------------------------|
| API Key          | Simple token, less secure               |
| Basic Auth       | Base64 username:password                |
| Bearer Token     | Passed in `Authorization` header        |
| OAuth 2.0        | Token-based, secure standard            |
| JWT              | JSON Web Tokens for stateless auth      |

---

## 🧰 Tools to Work With APIs

- **Postman** – API testing GUI
- **cURL** – Command-line tool
- **Swagger/OpenAPI** – Auto-generated documentation & UI
- **Insomnia** – Modern REST client
- **Mockoon** – Create mock APIs for testing

---

## 🛠️ Best Practices

1. Use nouns in endpoints: `/users`, not `/getUsers`
2. Version your API: `/api/v1/...`
3. Use appropriate HTTP methods
4. Always return meaningful status codes
5. Validate and sanitize input
6. Handle errors gracefully (`4xx`, `5xx`)
7. Secure with auth (OAuth, JWT)
8. Document everything with Swagger/OpenAPI
9. Enable pagination for lists
10. Apply rate limiting

---

## 🧠 API Interview Q&A

- **PUT vs PATCH**: PUT replaces entire resource, PATCH updates part.
- **401 vs 403**: 401 = Unauthenticated; 403 = Unauthorized.
- **REST vs SOAP**: REST is lightweight (JSON), SOAP is heavyweight (XML).
- **Idempotency**: Same request = same result (`GET`, `PUT`, `DELETE`).
- **HATEOAS**: Server returns links for next actions (advanced REST).
- **Caching**: Uses ETag, If-None-Match, Cache-Control headers.

---

## 🧪 Example: Create User API

```
POST /api/v1/users
Content-Type: application/json

{
  "name": "Alice",
  "email": "alice@example.com"
}

Response:
201 Created
Location: /api/v1/users/123
```

---

## 📦 API JSON Example

```json
{
  "id": 123,
  "name": "John Doe",
  "email": "john@example.com",
  "roles": ["admin", "editor"]
}
```

---

## 🔗 Useful Resources

- [Postman](https://postman.com)
- [Swagger Editor](https://editor.swagger.io/)
- [MDN HTTP Status Codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)
- [httpstatuses.com](https://httpstatuses.com)
- [JWT.io](https://jwt.io)

---

## 📌 Final Tips

- Learn to test in Postman + Swagger
- Be confident in designing REST APIs
- Prepare CRUD APIs and explain endpoints
- Practice real-world use cases

---
---
---
---

## 🧭 Table of Contents

- [API Fundamentals](#api-fundamentals)
- [Modern REST Architecture](#modern-rest-architecture)
- [HTTP Deep Dive](#http-deep-dive)
- [Complete Status Code Strategy](#complete-status-code-strategy)
- [Auth Systems (JWT, OAuth2)](#auth-systems-jwt-oauth2)
- [Designing Scalable APIs](#designing-scalable-apis)
- [Versioning, Pagination, Filtering](#versioning-pagination-filtering)
- [Testing & Tools](#testing--tools)
- [Rate Limiting, Caching, Headers](#rate-limiting-caching-headers)
- [Error Handling](#error-handling)
- [Security Best Practices](#security-best-practices)
- [Interview Focus: API Scenarios](#interview-focus-api-scenarios)
- [Real-World Patterns](#real-world-patterns)

---

## API Fundamentals

- API = Application Programming Interface
- Interfaces between 2 systems: clients (web/mobile) and backend (server/database)
- APIs define **contracts** (inputs, outputs, protocols)
- Key for: **microservices**, **CI/CD**, **frontend-backend integration**, **DevOps hooks**

---

## Modern REST Architecture

### 🔄 Statelessness
Each request is independent; no session data stored on server.

### 🌍 Resource-Based
Endpoints should represent **resources**, not actions.
- ✅ `/users/45`
- ❌ `/getUserById/45`

### 🧱 Representations
Client receives JSON (or XML) representation of resource.

### 📐 Uniform Interface
Use HTTP methods properly:
- `GET /users`
- `POST /users`
- `PUT /users/5`
- `DELETE /users/5`

---

## HTTP Deep Dive

| Concept       | Description                                   |
|---------------|-----------------------------------------------|
| Verb          | Action (`GET`, `POST`, etc.)                  |
| URL           | Resource endpoint                             |
| Headers       | Metadata (e.g., auth, content-type)           |
| Body          | JSON/XML payload (for `POST`, `PUT`, `PATCH`) |
| Status Code   | Response status (`200`, `404`, `422`, etc.)   |

---

## Complete Status Code Strategy

### ✅ Success Codes
- `200 OK` – Success
- `201 Created` – Resource created
- `202 Accepted` – Async processing
- `204 No Content` – Success, no response body

### ❌ Client Errors
- `400 Bad Request` – Invalid input
- `401 Unauthorized` – Missing/invalid token
- `403 Forbidden` – Authenticated but not allowed
- `404 Not Found` – Resource not found
- `409 Conflict` – Duplicate entry
- `422 Unprocessable Entity` – Validation fails

### 🔥 Server Errors
- `500 Internal Error` – App crash or misconfig
- `502/503` – Downstream service timeout/unavailable

---

## Auth Systems (JWT, OAuth2)

### 🔐 JWT (JSON Web Tokens)
- Stateless, encoded tokens
- Header.Payload.Signature
- Used for sessionless auth
- Secure with expiry and signature

### 🌐 OAuth2
- Used for delegated access (e.g., Google Login)
- Flow: Client → Authorization Server → Access Token

---

## Designing Scalable APIs

### ✅ Best Practices

- Use nouns: `/orders`, not `/createOrder`
- Version APIs: `/v1/products`
- Separate read vs write models if scale is needed (CQRS)

### 🔀 Filtering, Pagination, Sorting

```
GET /products?limit=10&page=2&sort=price&category=electronics
```

### 🔁 Idempotency

- `PUT` and `DELETE` must be idempotent
- Use **idempotency-keys** for `POST`

---

## Testing & Tools

- **Postman** – Manual testing & automation
- **Swagger/OpenAPI** – Contract-first design, auto-docs
- **Insomnia** – REST client
- **cURL** – Command-line API testing

---

## Rate Limiting, Caching, Headers

- Use `X-Rate-Limit`, `Retry-After`
- Enable client & proxy caching with:
  - `Cache-Control: max-age`
  - `ETag` and `If-None-Match`

---

## Error Handling

Use consistent error structure:

```json
{
  "status": 422,
  "error": "Validation Failed",
  "details": {
    "email": "Invalid format",
    "password": "Too short"
  }
}
```

Return specific messages — don't just say “something went wrong.”

---

## Security Best Practices

- Use HTTPS always
- Validate all input (headers, query, body)
- Use OAuth2/JWT over basic tokens
- Avoid sending secrets in URLs
- Sanitize error messages (don’t leak stack traces)
- Use **CORS** headers wisely

---

## Interview Focus: API Scenarios

- Design REST APIs for: User Signup, Booking System, eCommerce Cart
- Know CRUD mappings, status codes, and auth flows
- Explain scalability strategies: pagination, caching, versioning

---

## Real-World Patterns

- **Rate Limiter** (middleware)
- **Circuit Breaker** (for downstream resilience)
- **Bulkhead** (isolate failures per service)
- **Retry Logic** (exponential backoff for 5XX)
- **Logging + Monitoring**: API Gateway logs, Sentry, Prometheus

---

🧠 Just reading this will **make you interview-ready, system-design-ready, and production-ready** in API development — no more faking!
