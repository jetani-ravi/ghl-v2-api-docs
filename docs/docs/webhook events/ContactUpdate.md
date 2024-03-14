---
tags: [Webhook Events]
---

# Contact

Called whenever the specific fields in contact is updated

#### Schema

```json json_schema
{
  "type": "object",
  "properties": {
    "type": {
      "type": "string"
    },
    "locationId": {
      "type": "string"
    },
    "id": {
      "type": "string"
    },
    "address1": {
      "type": "string"
    },
    "city": {
      "type": "string"
    },
    "companyName": {
      "type": "string"
    },
    "country": {
      "type": "string"
    },
    "source": {
      "type": "string"
    },
    "dateAdded": {
      "type": "string"
    },
    "dateOfBirth": {
      "type": "string"
    },
    "dnd": {
      "type": "boolean"
    },
    "email": {
      "type": "string"
    },
    "name": {
      "type": "string"
    },
    "firstName": {
      "type": "string"
    },
    "lastName": {
      "type": "string"
    },
    "phone": {
      "type": "string"
    },
    "postalCode": {
      "type": "string"
    },
    "state": {
      "type": "string"
    },
    "tags": {
      "type": "array"
    },
    "website": {
      "type": "string"
    },
    "attachments": {
      "type": "array"
    },
    "assignedTo": {
      "type": "string"
    }
  }
}
```

#### Example

```json
{
  "type": "ContactUpdate",
  "locationId": "ve9EPM428h8vShlRW1KT",
  "id": "nmFmQEsNgz6AVpgLVUJ0",
  "address1": "3535 1st St N",
  "city": "ruDolomitebika",
  "state": "AL",
  "companyName": "Loram ipsum",
  "country": "DE",
  "source": "xyz form",
  "dateAdded": "2021-11-26T12:41:02.193Z",
  "dateOfBirth": "2000-01-05T00:00:00.000Z",
  "dnd": true,
  "email": "JohnDeo@gmail.comm",
  "name": "John Deo",
  "firstName": "John",
  "lastName": "Deo",
  "phone": "+919509597501",
  "postalCode": "452001",
  "tags": ["id magna sed Lorem", "Duis dolor commodo aliqua"],
  "website": "https://www.google.com/",
  "attachments": [],
  "assignedTo": "nmFmQEsNgz6AVpgLVUJ0"
}
```
