# Technical-test-iOS




## Endpoint

`POST https://staging---main-n7cgsmed7q-uc.a.run.app/ai/technical-test`

Send messages to the AI assistant and get responses back. Each `userID` gets its own isolated conversation session.

### Request Body

```json
{
  "userID": "candidate-123",
  "messages": [
    {
      "content": "Hello, how are you?",
      "localID": "8a5ac9d7-a8e4-486b-ab48-7b7c6db5d383"
    }
  ]
}
```

### Response

```json
{
  "userMessages": [
    {
      "_id": "e0ed...",
      "localID": "8a5ac9d7-a8e4-486b-ab48-7b7c6db5d383",
      "userID": "candidate-123",
      "sessionID": "abc1...",
      "role": "user",
      "content": "Hello, how are you?",
      "createdAt": "2025-02-05T12:00:00.000Z"
    }
  ],
  "assistantMessages": [
    {
      "_id": "6790...",
      "userID": "candidate-123",
      "sessionID": "abc1...",
      "role": "assistant",
      "content": "Hey! I'm doing great, thanks for asking...",
      "createdAt": "2025-02-05T12:00:04.000Z"
    }
  ]
}
```

### Reset Session

Send `[DELETE]` as the message content to clear your conversation history and start fresh.

```json
{
  "userID": "candidate-123",
  "messages": [{ "content": "[DELETE]" }]
}
```
