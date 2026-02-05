# Mission

Build the chat experience for Mira, an AI companion.

Copy the exact same experience you see on [this screen recording](https://github.com/user-attachments/assets/25cc1fb7-4a5e-4353-ba9a-271cff15cab9)


Mira should feel present, responsive, and alive, the kind of chat where you quickly forget you’re talking to a machine.

**BONUS**: Do you know that Mira can react to your messages? :wink:

# Endpoint

`POST https://staging---main-n7cgsmed7q-uc.a.run.app/ai/technical-test`

Send messages to the AI assistant and get responses back. Each `userID` gets its own isolated conversation session.

## Request Body

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

## Response

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

## Reset Session

Send `[DELETE]` as the message content to clear your conversation history and start fresh.

```json
{
  "userID": "candidate-123",
  "messages": [{ "content": "[DELETE]" }]
}
```

# Share your work

You want to share your work to us so we can review it.

Please **DO NOT** make it public and follow these steps:

## 1 - Fork the code in a private repository

You have to fork the current repository in your own github account as a **private** repository.

You can achieve this by using the `import` feature of github and use these values:

- **url**:`https://github.com/Amon-Studio/Technical-test-iOS.git`
- **repository name**: amon-technical-test-<your_github_nickname>
- **private**: true

## 2 - Clone your new repository

You can clone this new repository and push into it.

## 3 - Code ✍️

You can code, commit and push into this new repository.

## 4 - Add collaborators to your new repository

**WHEN YOU ARE READY** and want us to review your code:

You have to add these reviewers as collaborators to your repository:

- gautier-gdx

Finally, don’t forget to submit your **GitHub URL** AND **a screen recording of 1min max** containing your final solution, in the email you received about the case study.

From this stage, we consider you have finished the task!

## 5 - Chill & Wait

Then it's us to reach you after the review is done.
Just chill!
