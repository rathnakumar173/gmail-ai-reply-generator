# Email Writer Assistant

A Chrome/Brave extension that adds an **AI Reply** button to Gmail. It calls a **Spring Boot** backend that integrates with **Google Gemini** to generate replies in different tones.

## ✨ Features
- AI Reply button in Gmail
- Tones: Professional, Friendly, Polite, Short, Casual
- Spring Boot backend using Gemini API

## 📁 Project Structure
-/extension # Browser Extension (Manifest V3)
-/backend # Java Spring Boot Service

## 🚀 Getting Started

### Backend Setup
1. Create file: `backend/src/main/resources/application.properties`
2. Add: gemini.api.url=https://generativelanguage.googleapis.com/v1/models/gemini-pro:generateContent?key=

gemini.api.key=YOUR_API_KEY_HERE
server.port=8080

3. Run: ./mvnw spring-boot:run
4.
### Extension Setup
1. Open: `chrome://extensions` (or `brave://extensions`)
2. Enable **Developer Mode**
3. Click **Load Unpacked**
4. Select the `extension/` folder
5. Open Gmail → Compose → Click **AI Reply**

## 🔐 Important
- Do **NOT** commit your real API key.
- Use `application-example.properties` in repo instead.

## 📝 License
MIT

