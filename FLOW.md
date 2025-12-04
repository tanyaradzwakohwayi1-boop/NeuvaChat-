

App Flow – NeuvaChat

This document explains how NeuvaChat works from start to finish, showing developers the full message flow inside the app.


---

1️⃣ App Launch

When the user opens NeuvaChat:

The app loads the main chat screen

Initializes the message list (empty on first launch)

Checks if the API key is set in the App Inventor blocks

Prepares the UI components (input box, send button, chat area)



---

2️⃣ User Sends a Message

When the user types a message and presses Send:

1. The message is added to the chat list (as "User")


2. The app calls the API Request block with:

User message

Model: gpt-4o-mini

Temperature and max tokens



3. While waiting, the app displays a “Typing…” indicator.




---

3️⃣ API Request

The app sends a POST request to the ChatGPT API:

https://api.openai.com/v1/chat/completions

The body includes:

Model name

User message

System instructions (optional)

Response formatting settings


The request is handled using the Web Component in MIT App Inventor.


---

4️⃣ API Response

When the API returns a result:

The “Typing…” indicator disappears

The assistant message is extracted from choices[0].message.content

The assistant message is added to the chat list (as "AI")

The chat UI updates to show the conversation


If the API fails (timeout, invalid key, network error):

The app displays an error message in the chat

Suggests retrying or checking the API key



---

5️⃣ Displaying the Messages

Messages are shown inside a scrollable layout:

User messages aligned right

AI messages aligned left

Timestamp automatically generated

Chat scrolls to the newest message



---

6️⃣ New Conversation

When the user taps Clear Chat:

All messages are removed

The chat resets to a fresh start

App remains connected to the API



---

7️⃣ Closing the App

When the user exits:

No data is stored (unless offline history is added later)

On next launch, the chat starts clean



---

Summary

NeuvaChat follows a simple, clean, and predictable flow:

Launch → User Message → API Request → API Response → Display → Repeat


---

