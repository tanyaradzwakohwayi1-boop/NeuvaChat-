


✨ DESIGN.md — NeuvaChat App Design Document

🎨 1. Design Philosophy

NeuvaChat is designed to be:

Fast

Clean

Beginner-friendly

Modern and minimalistic

Consistent across Android, Web, and Desktop


The interface must feel light, responsive, and intuitive even on low-end devices.


---

📱 2. App Layout Structure

Top-Level Screens

The app consists of the following screens:

1. Splash Screen

Shows the NeuvaChat logo

Loads user session / app data



2. Onboarding Screen

Welcome message

Request permissions (internet, storage optional)

Continue button



3. Login / API Key Screen

User enters:

OpenAI API key

(Optional) Model selection


Validate key

Save securely



4. Home / Chat Screen

Chat history list (scrollable)

Main chat area

User input box + send button

Settings shortcut



5. Settings Screen

API key management

Theme selection (Light / Dark)

Clear chat history

About section





---

🧩 3. Component Design

Chat Bubbles

User messages: right-aligned, blue bubble

AI messages: left-aligned, white or grey bubble

Should support:

Text

Code blocks

Markdown

Images (future update)



Input Bar

Text field

Microphone button (future)

“Send” icon

Auto-expand on long messages



---

🎨 4. Color System

Primary: #4C7EFF
Secondary: #FFFFFF
Accent: #A5B4FC
Error: #EF4444
Background Light: #F5F7FA
Background Dark: #0F172A


---

🔤 5. Typography

Title: Bold, 22sp

Section headers: 18sp

Body text: 14–16sp

Mono text for code: 14sp


Font family: Inter or Roboto (depending on device availability)


---

🔧 6. UI Flow Diagram (Text Version)

Splash → Onboarding → Login → Home(Chat)
                                  ↘
                                   Settings


---

🧱 7. Modular Screen Breakdown

Splash Activity

Logo centered

2-second fade animation


Onboarding Activity

Welcome text

“Continue” button


Login/API Key Activity

Field for API key

“Test Connection”

“Save & Continue”


Chat Activity

Chat recycler view

AI typing indicator

Overflow menu


Settings Activity

Reset / Clear Data

Theme toggle

About app



---

🚀 8. Performance Requirements

Load chat instantly

Smooth scrolling

Caching for messages

Offline placeholder states

Minimal animations for speed



---

📦 9. Deliverables for MIT App Inventor

Screen XML equivalents

Component properties

Blocks layout for:

API calls

Chat display

Settings storage

Error handling




---

🏁 End of DESIGN.md




