---
tags: [Webhook Events]
---

# App

Called whenever an app is installed

#### Schema

```json json_schema
{
  "type": "object",
  "properties": {
    "type": {
      "type": "string"
    },
    "appId": {
      "type": "string"
    },
    "companyId": {
      "type": "string"
    },
    "locationId": {
      "type": "string"
    },
    "userId": {
      "type": "string"
    }
  }
}
```

- Note: The User ID and Company ID may be available when a new token is generated. In case of app installation via future locations, you may not get these fields.

#### Example

- For Location Level App Install

```json
{
  "type": "INSTALL",
  "appId": "ve9EPM428h8vShlRW1KT",
  "locationId": "otg8dTQqGLh3Q6iQI55w",
  "companyId": "otg8dTQqGLh3Q6iQI55w",
  "userId": "otg8dTQqGLh3Q6iQI55w"
}
```

- For Agency Level App Uninstall

```json
{
  "type": "INSTALL",
  "appId": "ve9EPM428h8vShlRW1KT",
  "companyId": "otg8dTQqGLh3Q6iQI55w"
}
```
