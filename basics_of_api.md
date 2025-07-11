# HTTP Status Codes & API Basics

This document provides a concise yet comprehensive summary of HTTP status codes and core API concepts, ideal for quick reference and interviews.

---

## 📘 HTTP Basics

- **HTTP** (HyperText Transfer Protocol) is the protocol used to transfer data across the internet.
- **API** (Application Programming Interface) allows two servers/systems to exchange data.
- **CRUD Operations** (mapped to HTTP methods):
  - **C**reate → `POST`
  - **R**ead → `GET`
  - **U**pdate → `PUT` / `PATCH`
  - **D**elete → `DELETE`

---

## 🔢 HTTP Status Code Categories

| Category | Range  | Meaning                         |
|----------|--------|----------------------------------|
| 1XX      | 100–199 | Informational (request received, continue process) |
| 2XX      | 200–299 | Success (request received, understood, accepted) |
| 3XX      | 300–399 | Redirection (further action needed) |
| 4XX      | 400–499 | Client Error (request incorrect) |
| 5XX      | 500–599 | Server Error (server failed to fulfill valid request) |

---

## ✅ 1XX - Informational Responses

### `100 Continue`
- Sent by server to indicate the initial part of the request is received and client should continue.
- **Use Case**: Large file upload (e.g., 4GB). Server checks if it’s acceptable before proceeding.

### `101 Switching Protocols`
- Indicates server agrees to switch protocols (e.g., HTTP → WebSocket).
- **Use Case**: Client requests protocol upgrade.

---

## 🟩 2XX - Success

| Code | Meaning | Description |
|------|---------|-------------|
| `200 OK` | Request succeeded | Action was successful. Be cautious: success may not always mean the action had the intended effect (e.g., user not created). |
| `201 Created` | Resource created | New resource has been created. Response includes `Location` header pointing to the resource. |
| `202 Accepted` | Request accepted but processing not complete | Used when processing is delayed (e.g., background job). Client may send `Prefer` header to tell how long it's willing to wait. |
| `203 Non-Authoritative Information` | Metadata not from origin server | Response is OK, but some data may be from cache or third party. |
| `204 No Content` | Request succeeded but no content returned | Typically sent for `PUT` or `DELETE` operations. No body in response. Useful when action is done but there’s no representation to send back. |
| `205 Reset Content` | Client should reset the document view | Sent when form submission should reset UI. |
| `206 Partial Content` | Partial GET successful | Used when serving partial content using range headers. Example: video streaming or download resuming. |

---

## 🧾 API Data Formats

### 🟦 JSON (JavaScript Object Notation)
- Lightweight data-interchange format.
- Format: `"key": "value"`
- Widely used in REST APIs.
- Smaller and easier to parse than XML.

### 🟨 XML (Extensible Markup Language)
- Used in **SOAP APIs**.
- Tags don’t carry inherent meaning.
- Verbose format, not commonly used in modern RESTful systems.

---

## 📬 REST vs SOAP

| Feature       | REST (JSON)          | SOAP (XML)             |
|---------------|----------------------|-------------------------|
| Format        | JSON                 | XML                    |
| Usage         | Most modern APIs     | Legacy systems         |
| Verbosity     | Lightweight          | Heavy and strict       |
| Flexibility   | High                 | Rigid specifications   |

---

## 🧪 Using `PUT` for Update

- `PUT` is similar to SQL `UPDATE`.
- Used to **replace** or **update** a resource.
- Can update part of a resource by sending only that part.
- Example: Updating 1 entry out of 5 mapped to an ID without resending the full object.

---

## 🎯 Key Takeaways

- Not all `200 OK` responses mean your action was successful logically (e.g., user creation failed silently).
- Use appropriate status codes for clarity and proper API design.
- REST APIs favor **clarity**, **lightweight communication**, and **statelessness**.
- **Use correct headers** (like `Location`, `Prefer`) to enhance communication between client and server.

---

## 📚 Resources for Practice

- [Postman](https://www.postman.com/) – for testing REST APIs
- [HTTP Status Codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status) – full list on MDN

