# REST API Guide

**Document ID:** API-001  
**Version:** 1.0  
**Status:** Draft (Portfolio Sample)

---

# Purpose

This guide describes the REST APIs available in the FinCore Platform for managing customers, accounts, products, and transactions.

> **Note:** This document is a fictional portfolio sample created to demonstrate API documentation skills.

---

# Base URL

```
https://api.fincore.com/v1
```

---

# Authentication

All API requests require OAuth 2.0 Bearer Token authentication.

Example:

```http
Authorization: Bearer <access_token>
```

---

# Common Request Headers

| Header | Description |
|---------|-------------|
| Authorization | OAuth 2.0 Bearer Token |
| Content-Type | application/json |
| Accept | application/json |
| Correlation-ID | Unique request identifier |

---

# Customer API

## Create Customer

### Endpoint

```http
POST /customers
```

### Request

```json
{
  "customerId": "100245",
  "firstName": "John",
  "lastName": "Smith",
  "email": "john.smith@example.com"
}
```

### Success Response

```json
{
  "status": "SUCCESS",
  "message": "Customer created successfully."
}
```

---

## Get Customer

### Endpoint

```http
GET /customers/{customerId}
```

### Example

```http
GET /customers/100245
```

---

# Account API

## Create Account

```http
POST /accounts
```

### Request

```json
{
  "customerId": "100245",
  "accountType": "Savings",
  "currency": "USD"
}
```

---

# Product API

## List Products

```http
GET /products
```

Returns all available banking products.

---

# HTTP Status Codes

| Code | Description |
|------|-------------|
| 200 | Success |
| 201 | Resource Created |
| 400 | Bad Request |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |
| 409 | Conflict |
| 500 | Internal Server Error |

---

# Error Response

```json
{
  "code": "INVALID_REQUEST",
  "message": "Customer ID is required."
}
```

---

# Best Practices

- Use HTTPS for all requests.
- Validate request payloads.
- Include Correlation-ID in every request.
- Handle HTTP status codes appropriately.
- Protect access tokens.

---

# Related Documentation

- Banking Platform Overview
- Interface Specification
- Kafka Streaming Guide
- Swagger/OpenAPI Guide
