

# NeuvaChat – Full Project Specification

## 1. Overview
NeuvaChat is an open-source AI chat application designed to be simple, fast, and modern.  
The app is built using MIT App Inventor and the ChatGPT API.  
This specification contains the full technical plan for building NeuvaChat from the foundation to final features.



## 2. Core Features (MVP)
The first version of NeuvaChat will include:

### ✅ AI Chat
- ChatGPT-powered messaging  
- Sends user input to API  
- Receives AI reply and displays it  
- Message history visible in chat screen  

### ✅ Clean UI
- Simple 1-screen layout  
- User bubble (right)  
- AI bubble (left)  
- Colors: white background, purple accents  

### ✅ Error Handling
- “No internet” message  
- API error message  
- Loading indicator  



## 3. App Structure
### Screens
1. **Screen1 (MainChat)**
   - TextBox for user input  
   - Send button  
   - Chat layout (vertical scroll)  

### Components
- Web Component (for API call)  
- Notifier Component (for errors)  
- TinyDB (optional for message saving)  



## 4. API Integration
### Endpoint

https://api.openai.com/v1/chat/completions

### Method

POST

### Headers
- Authorization: Bearer YOUR_API_KEY  
- Content-Type: application/json  

### Body Template

{ "model": "gpt-4.1-mini", "messages": [ {"role": "user", "content": "USER_MESSAGE_HERE"} ] }



## 5. Message Handling Flow
1. User types a message  
2. App displays user bubble  
3. App sends request to API  
4. Shows “Loading…” placeholder  
5. API returns a reply  
6. App displays AI bubble  
7. Clears loading placeholder  



## 6. Future Features (Phase 2)
### ⭐ Saved Chat History  
### ⭐ Theme Mode  
### ⭐ Voice Input  
### ⭐ Export Conversation  
### ⭐ Chat Categories  
### ⭐ Offline Mode (stored prompts)  



## 7. Long-Term Goals (Phase 3)
### 🚀 NeuvaChat Pro  
- Faster API  
- Smart prompts  
- Custom AI personalities  
- Local database  
- Cloud sync  
- Pro themes  



## 8. Security
- Users must enter their own API key  
- App never uploads API key anywhere  
- No tracking  
- All messages stored locally only  



## 9. Open-Source Rules
- Anyone can help build  
- Contributors submit pull requests on GitHub  
- No usage of paid assets  
- All code must remain open  



## 10. Purpose
NeuvaChat’s main purpose is to be:
- A beginner-friendly AI chat project  
- Easy for developers to collaborate on  
- A stepping stone to larger AI apps  



**End of specification.**

