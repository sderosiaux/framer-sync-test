---
title: Configuration Guide
description: Learn how to configure the platform for your needs
section: Guides
subsection: Setup
order: 2
difficulty: Intermediate
estimatedTime: 20 minutes
---

# Configuration Guide

Customize the platform to match your requirements with these configuration options.

## Configuration File

The main configuration is stored in `config.json` at the root of your project:

```json
{
  "app": {
    "name": "My Application",
    "port": 3000,
    "environment": "development"
  },
  "database": {
    "type": "postgres",
    "host": "localhost",
    "port": 5432
  },
  "features": {
    "authentication": true,
    "analytics": false,
    "notifications": true
  }
}
```

## Environment-Specific Settings

Create separate configuration files for different environments:

- `config.development.json`
- `config.staging.json`
- `config.production.json`

The platform automatically loads the appropriate file based on `NODE_ENV`.

## Security Configuration

### Authentication Settings

Configure authentication providers:

```json
{
  "auth": {
    "providers": ["google", "github"],
    "sessionDuration": "7d",
    "requireEmailVerification": true
  }
}
```

### CORS Configuration

Set up Cross-Origin Resource Sharing:

```json
{
  "cors": {
    "origin": ["https://yourdomain.com"],
    "credentials": true,
    "methods": ["GET", "POST", "PUT", "DELETE"]
  }
}
```

## Advanced Options

For advanced users, additional configuration options are available in the [Advanced Configuration](../advanced/configuration.md) guide.
