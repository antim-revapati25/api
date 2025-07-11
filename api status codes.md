# 🌐 HTTP Status Codes & API Basics

A complete reference to HTTP status codes and core API concepts. Suitable for developers and interview preparation. Includes use cases and quick comparisons.

---

## 📘 HTTP & API Basics

- **HTTP (Hypertext Transfer Protocol)** is used to transfer data over the web.
- **API (Application Programming Interface)** allows different systems to communicate.
- **CRUD Operations** in REST API:

| Operation | HTTP Method |
|-----------|-------------|
| Create    | POST        |
| Read      | GET         |
| Update    | PUT / PATCH |
| Delete    | DELETE      |

---

## 🔢 HTTP Status Code Classes

| Class | Code Range | Purpose                       |
|-------|------------|-------------------------------|
| 1XX   | 100–199    | Informational                 |
| 2XX   | 200–299    | Success                       |
| 3XX   | 300–399    | Redirection                   |
| 4XX   | 400–499    | Client Errors                 |
| 5XX   | 500–599    | Server Errors                 |

---

## 🟦 1XX – Informational

| Code | Message               | Description |
|------|------------------------|-------------|
| `100` | Continue              | Initial part of the request is OK, continue sending. |
| `101` | Switching Protocols   | Server switching protocols as requested. |
| `102` | Processing (WebDAV)   | Server has accepted but not completed the request. |
| `103` | Early Hints           | Used for preloading resources before final response. |

---

## ✅ 2XX – Success

| Code | Message                   | Description |
|------|---------------------------|-------------|
| `200` | OK                        | Request succeeded. |
| `201` | Created                   | Resource created, often includes `Location` header. |
| `202` | Accepted                  | Request accepted for processing, but not completed yet. |
| `203` | Non-Authoritative Info    | Meta-information returned is not from origin server. |
| `204` | No Content                | Request processed, no content to return. |
| `205` | Reset Content             | Tells client to reset the view (e.g., clear form). |
| `206` | Partial Content           | Partial response to a range request (e.g., file download). |
| `207` | Multi-Status (WebDAV)     | Multiple status codes for batch operations. |
| `208` | Already Reported (WebDAV) | Avoid repeated listing of internal members. |
| `226` | IM Used                   | Server has fulfilled request using instance manipulation. |

---

## 🔁 3XX – Redirection

| Code | Message                   | Description |
|------|---------------------------|-------------|
| `300` | Multiple Choices         | Multiple options for the resource. |
| `301` | Moved Permanently        | Resource permanently moved to a new URI. |
| `302` | Found (Previously Moved Temporarily) | Temporary redirection. |
| `303` | See Other                | Redirect using `GET` method to another URI. |
| `304` | Not Modified             | Cached version is still valid. |
| `305` | Use Proxy (Deprecated)   | Resource must be accessed via proxy. |
| `307` | Temporary Redirect       | Same method used, temporarily moved. |
| `308` | Permanent Redirect       | Same method used, resource moved permanently. |

---

## 🚫 4XX – Client Errors

| Code | Message                   | Description |
|------|---------------------------|-------------|
| `400` | Bad Request              | Malformed syntax or invalid request. |
| `401` | Unauthorized             | Authentication required. |
| `402` | Payment Required         | Reserved for future use (used in APIs for limited services). |
| `403` | Forbidden                | Server understood, but refuses to authorize. |
| `404` | Not Found                | Resource not found. |
| `405` | Method Not Allowed       | Method not allowed on this endpoint. |
| `406` | Not Acceptable           | Resource not capable of returning acceptable data. |
| `407` | Proxy Authentication Required | Similar to 401, but for proxies. |
| `408` | Request Timeout          | Server timed out waiting for request. |
| `409` | Conflict                 | Request conflict with server state (e.g., duplicate data). |
| `410` | Gone                     | Resource no longer available and won’t return. |
| `411` | Length Required          | Missing Content-Length header. |
| `412` | Precondition Failed      | Preconditions not met. |
| `413` | Payload Too Large        | Request body too large. |
| `414` | URI Too Long             | URI exceeds max length. |
| `415` | Unsupported Media Type   | Media type not supported (e.g., expecting JSON). |
| `416` | Range Not Satisfiable    | Invalid range in request. |
| `417` | Expectation Failed       | Server can't meet the expectation. |
| `418` | I'm a Teapot 🫖          | Easter egg from [RFC 2324](https://tools.ietf.org/html/rfc2324). |
| `422` | Unprocessable Entity     | Server understands data but can't process it (common in validation errors). |
| `429` | Too Many Requests        | Rate limit exceeded. |
| `431` | Request Header Fields Too Large | Header too large to process. |

---

## 🛑 5XX – Server Errors

| Code | Message                   | Description |
|------|---------------------------|-------------|
| `500` | Internal Server Error    | Generic error, something failed on server. |
| `501` | Not Implemented          | Method not supported. |
| `502` | Bad Gateway              | Invalid response from upstream server. |
| `503` | Service Unavailable      | Server is down or overloaded. |
| `504` | Gateway Timeout          | Upstream server failed to respond in time. |
| `505` | HTTP Version Not Supported | HTTP version not supported. |
| `507` | Insufficient Storage (WebDAV) | Server out of storage. |
| `511` | Network Authentication Required | Client must authenticate to gain network access. |

---

## 📦 API Data Format Summary

| Format | Description                     |
|--------|---------------------------------|
| JSON   | JavaScript Object Notation, compact, modern |
| XML    | Extensible Markup Language, verbose, used in SOAP |
| REST   | Architectural style, uses JSON and HTTP |
| SOAP   | Protocol using XML, strict structure |

---

## 📌 Real-World Examples

- `200 OK`: Data retrieved or operation completed successfully.
- `201 Created`: New user created, returns `Location` header.
- `204 No Content`: User deleted, no response body needed.
- `400 Bad Request`: Missing field in request body.
- `401 Unauthorized`: Missing/invalid token.
- `404 Not Found`: Requested user ID doesn't exist.
- `409 Conflict`: Email already exists.
- `500 Internal Server Error`: Server crashed or unknown error.

---

## 🧪 Tools to Practice

- [Postman](https://www.postman.com/) – Test and simulate API calls.
- [httpstatuses.com](https://httpstatuses.com) – Browse all status codes.
- [MDN HTTP Docs](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status) – Mozilla Developer Network.

---

📝 **Pro Tip**: Always use correct status codes in APIs. They are essential for debugging, user experience, and RESTful design.

