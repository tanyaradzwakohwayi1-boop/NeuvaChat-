

NeuvaChat API Documentation

This document explains how NeuvaChat connects to the ChatGPT API using MIT App Inventor.


---

🔑 1. API Endpoint

NeuvaChat sends requests to:

https://api.openai.com/v1/chat/completions


---

🔧 2. Required HTTP Headers

NeuvaChat must include:

Content-Type: application/json
Authorization: Bearer YOUR_API_KEY

Replace YOUR_API_KEY with your real key.


---

📤 3. Request Format (JSON)

NeuvaChat sends the user's message using this JSON body:

{
  "model": "gpt-4o-mini",
  "messages": [
    { "role": "system", "content": "You are NeuvaChat, a helpful AI assistant." },
    { "role": "user", "content": "USER_MESSAGE_HERE" }
  ]
}


---

📥 4. Response Format

OpenAI returns a JSON response.
The important part for NeuvaChat is:

response.choices[0].message.content

This contains the bot's reply.


---

🔄 5. App Inventor Blocks Overview

In MIT App Inventor:

1. Set Web1.Url to the API endpoint


2. Set Web1.RequestHeaders to:

"Content-Type: application/json"

Authorization: Bearer <your API key>



3. Use Web1.PostText to send the JSON request


4. Use Web1.GotText to extract the AI response



Pseudocode:

When SendButton.Click:
    Build JSON
    Web1.PostText(JSON)

When Web1.GotText:
    response ← extract choices[0].message.content
    Add new message to chat


---

🧪 6. Test Request Example

If you send:

{ "model": "gpt-4o-mini", "messages": [{ "role": "user", "content": "Hello!" }] }

The response will look like:

{
  "id": "...",
  "choices": [
    {
      "index": 0,
      "message": {
        "role": "assistant",
        "content": "Hi! How can I help you today?"
      }
    }
  ]
}


---

🔐 7. Security Guidelines

Never expose your API key publicly

Do not hard-code the key inside shared project files

Store API keys privately in App Inventor:

Use a hidden text field or secure input block


If your key is ever leaked → regenerate immediately



---

🎯 8. Summary

NeuvaChat uses:

✔ App Inventor Web Component
✔ JSON POST request
✔ ChatGPT "gpt-4o-mini" model
✔ Extracted assistant response
✔ Chat-style UI


