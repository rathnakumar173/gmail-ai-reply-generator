# Gmail AI Reply Generator ✉️🤖

A Chrome/Brave browser extension that adds an **AI-powered "AI Reply" button** directly inside the Gmail interface.  
When clicked, it sends the current email content to a **Spring Boot backend**, which uses **Google Gemini API** to generate a context-aware reply in your chosen tone.

---

## 🛠 Tech Stack

| Component | Technology |
|----------|------------|
| Browser Extension | JavaScript (Manifest V3), DOM Injection |
| Backend | Spring Boot, REST API |
| AI Model | Google Gemini API |
| Languages Used | Java, JavaScript |

---

## ✨ Features

- Seamlessly injects an **AI Reply** button inside Gmail compose window.
- Generates **professional, polite, or tone-aware replies**.
- Fully integrated **Spring Boot backend** that calls Google Gemini.
- Automatic insertion of generated reply into Gmail compose editor.
- Clean, lightweight, and **easy to set up locally**.
- Browser-extension is **non-invasive** — no UI redesign.

---

## 📂 Project Structure

/gmail-ai-reply-generator
│
├── /extension # Chrome Extension (Manifest V3)
│ ├── content.js # Injects "AI Reply" button into Gmail UI
│ └── manifest.json
│
└── /backend # Spring Boot Backend
├── EmailGeneratorController.java
├── EmailGeneratorService.java
└── application.properties (example provided)


---

## 🎯 How It Works (Architecture)

Gmail UI (Extension)
│
│ (email content + tone)
▼
Spring Boot Backend (REST API)
│
│ (prompt)
▼
Google Gemini API
│
│ (generated reply text)
▼
Reply automatically appears in Gmail compose box


---

## 🚀 Getting Started

### 1) Backend Setup (Spring Boot)

**Create configuration file:**

backend/src/main/resources/application.properties

Add: gemini.api.key=YOUR_API_KEY_HERE
server.port=8080


Run the application:
```bash
./mvnw spring-boot:run


2) Extension Setup (Chrome/Brave)

1.Open your browser and go to: chrome://extensions

2.Enable Developer Mode

3.Click Load Unpacked

4.Select the extension/ folder

5.Open Gmail → Compose → AI Reply button will appear automatically.

🔐 Security Note

Do not commit your real Gemini API key.

A application-example.properties template is included.

🔐 Security Note

Do not commit your real Gemini API key.

A application-example.properties template is included.

📝 License

This project is licensed under the MIT License.




