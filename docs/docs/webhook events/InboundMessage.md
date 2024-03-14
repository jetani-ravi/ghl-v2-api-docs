---
tags: [Webhook Events]
---

# InboundMessage

Called whenever a contact sends a message to the user.

| Channel   |
| --------- |
| Call      |
| SMS       |
| GMB       |
| FB        |
| IG        |
| Email     |
| Live Chat |

#### Message Schema

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
    "attachments": {
      "type": "array"
    },
    "body": {
      "type": "string"
    },
    "contactId": {
      "type": "string"
    },
    "contentType": {
      "type": "string"
    },
    "conversationId": {
      "type": "string"
    },
    "dateAdded": {
      "type": "string"
    },
    "direction": {
      "type": "string"
    },
    "messageType": {
      "type": "string"
    },
    "messageId": {
      "type": "string"
    },
    "userId": {
      "type": "string"
    }
  }
}
```

#### Example(Message)

```json
{
  "type": "InboundMessage",
  "locationId": "l1C08ntBrFjLS0elLIYU",
  "attachments": [],
  "body": "This is a test message",
  "contactId": "cI08i1Bls3iTB9bKgFJh",
  "contentType": "text/plain",
  "conversationId": "fcanlLgpbQgQhderivVs",
  "dateAdded": "2021-04-21T11:31:45.750Z",
  "direction": "inbound",
  "messageType": "SMS"
}
```

#### Email Message Schema

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
    "attachments": {
      "type": "array"
    },
    "body": {
      "type": "string"
    },
    "contactId": {
      "type": "string"
    },
    "conversationId": {
      "type": "string"
    },
    "dateAdded": {
      "type": "string"
    },
    "direction": {
      "type": "string"
    },
    "messageType": {
      "type": "string"
    },
    "emailMessageId": {
      "type": "string"
    },
    "threadId": {
      "type": "string"
    },
    "provider": {
      "type": "string"
    },
    "to": {
      "type": "string"
    },
    "cc": {
      "type": "string"
    },
    "bcc": {
      "type": "string"
    },
    "userId": {
      "type": "string"
    }
  }
}
```

#### Example(Email)

```json
{
  "type": "InboundMessage",
  "locationId": "kF4NJ5gzRyQF2gKFD34G",
  "body": "<div style=\"font-family: verdana, geneva; font-size: 11pt;\">Testing Email Notification</div>",
  "contactId": "3bN9f8LYJFG8F232XMUbfq",
  "conversationId": "yCdNo6pwyTLYKgg6V2gj",
  "dateAdded": "2024-01-12T12:59:04.045Z",
  "direction": "inbound",
  "messageType": "Email",
  "emailMessageId": "sddfDSF3G56GHG",
  "from": "Internal Notify <sample@email.service>",
  "threadId": "sddfDSF3G56GHG",
  "to": ["testprasath95@gmail.com"]
}
```

##### For listening to inbound messages

You need to change the Messaging webhook to -

<https://services.leadconnectorhq.com/conversations/providers/twilio/inbound_message>

You can find it inside your Twilio Account -

`Phone Numbers` > `Active Number` > `Click on the number` > `Messaging` > `A Message comes in`

If you want to revert, here's the old messaging webhook url -

<https://services.leadconnectorhq.com/appengine/twilio/incoming_message>
