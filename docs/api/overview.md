---
title: API Overview
description: Introduction to the platform API and available endpoints
section: API Reference
order: 1
apiVersion: v2
deprecated: false
---

# API Overview

Our REST API provides programmatic access to all platform features.

## Base URL

```
https://api.example.com/v2
```

## Authentication

All API requests require authentication using Bearer tokens:

```bash
curl -H "Authorization: Bearer YOUR_API_KEY" \
  https://api.example.com/v2/users
```

## Request Format

The API accepts JSON payloads for POST and PUT requests:

```bash
curl -X POST \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"name": "John Doe", "email": "john@example.com"}' \
  https://api.example.com/v2/users
```

## Response Format

All responses are returned in JSON format:

```json
{
  "success": true,
  "data": {
    "id": "123",
    "name": "John Doe",
    "email": "john@example.com"
  },
  "meta": {
    "timestamp": "2025-01-15T10:30:00Z"
  }
}
```

## Error Handling

Errors include a status code and descriptive message:

```json
{
  "success": false,
  "error": {
    "code": "INVALID_REQUEST",
    "message": "Email address is required",
    "field": "email"
  }
}
```

## Rate Limiting

- **Standard Plan**: 1,000 requests per hour
- **Pro Plan**: 10,000 requests per hour
- **Enterprise**: Custom limits

Rate limit information is included in response headers:

```
X-RateLimit-Limit: 1000
X-RateLimit-Remaining: 999
X-RateLimit-Reset: 1642251600
```

## Available Endpoints

Explore our endpoint documentation:

- [Users API](./users.md)
- [Projects API](./projects.md)
- [Authentication API](./auth.md)
