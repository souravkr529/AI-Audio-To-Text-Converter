# 🎙️ AI Audio To Text Converter
### The Secure, Private, and Free Web-Based Transcriber

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Privacy: High](https://img.shields.io/badge/Privacy-Local_Only-green.svg)
![AI Model: Gemini 2.0](https://img.shields.io/badge/AI_Model-Gemini_2.0_Flash-blueviolet.svg)
![Platform: Web](https://img.shields.io/badge/Platform-Browser_Based-orange)

**AI Audio To Text Converter** is a next-generation transcription tool designed for **absolute privacy** and **zero latency**. Unlike other services that upload your audio to a third-party server, this tool runs entirely in your browser. It connects **directly** to Google's powerful Gemini AI using your own API key, ensuring your data never touches a middleman.

---

## 🔒 Security Architecture: How Your Key & Data Are Safe

We utilize a **Bring Your Own Key (BYOK)** architecture. This is the gold standard for privacy-conscious AI tools.

### 🛡️ The "Zero-Server" Guarantee
*   **No Database**: We have no database to store your audio or your keys.
*   **No Backend**: There is no "server" sitting between you and Google.
*   **Client-Side Storage**: Your API Key is saved strictly in your browser's `localStorage`. It persists on **your device only**.
*   **Direct Tunnel**: When you transcribe, the request goes from `Your User Device` ➔ `Google Servers`. It cannot be intercepted by us.

### 🔐 Input Hardening
We have implemented military-grade input validation:
*   **Magic Bytes Detection**: Prevents malware from disguising itself as audio files.
*   **Regex Validation**: Ensures only valid Google API Key formats (`AIza...`) are accepted.
*   **XSS Sanitization**: All inputs and outputs are sanitized to prevent script injection attacks.

---

## 🌊 Workflow Diagram

Here is how your data flows securely through the system:

```mermaid
graph LR
    User((👤 You))
    
    subgraph Browser_Safe_Zone ["🔒 Secure Browser Environment"]
        Browser[("💻 Web App")]
        KeyStore[["🔑 LocalStorage"]]
    end

    subgraph Google ["☁️ Google Cloud"]
        Gemini[/"🧠 Gemini AI"\]
    end

    User -->|"1. Input Key"| Browser
    Browser -.->|"Save Key"| KeyStore
    User -->|"2. Upload Audio"| Browser
    Browser ==>"3. Secure Direct Request"==> Gemini
    Gemini ==>"4. Return Text"==> Browser
    Browser -->|"5. Display"| User
```

---

## 🌟 Key Features

*   **⚡ Blazing Fast**: Powered by Gemini 2.0 Flash, one of the fastest models in the world.
*   **🗣️ Speaker Verification**: Automatically detects and separates different speakers (Speaker 1, Speaker 2).
*   **🌍 Multilingual**: auto-detects and transcribes English, Hindi, Spanish, French, and 100+ others.
*   **📱 Mobile Optimized**: A responsive UI that works perfectly on iOS, Android, and Desktop.
*   **💸 100% Free to Use**: Since you use your own free Google Key, you pay nothing to us.

---

## 🚀 Quick Start Guide

### Step 1: Get Your Free Key
1.  Go to [Google AI Studio](https://aistudio.google.com/app/apikey).
2.  Click **"Create API Key"**.
3.  Copy the key (starts with `AIza...`).

### Step 2: Use the Converter
1.  Open the [Live Tool](https://souravkr529.github.io/AI-Audio-To-Text-Converter/).
2.  Click **"Enter API Key"** and paste your key.
3.  **Drag & Drop** your audio file.
4.  Watch the AI convert it to text in seconds!

---

## 🛠️ Technical Stack

*   **Frontend**: HTML5, Vanilla JavaScript (ES6+)
*   **Styling**: TailwindCSS (CDN)
*   **AI Engine**: Google Gemini API (REST)
*   **Security**: Content Security Policy (CSP), Input Sanitization

## 🙋‍♀️ FAQ

**Q: Can you see my API Key?**
A: **No.** Your key is stored in your browser's local cache. If you clear your browser history, the key is gone. We have no access to it.

**Q: Is my audio uploaded to your server?**
A: **No.** We do not have a server. The audio travels directly from your computer to Google for processing and then straight back to you.

**Q: What audio formats are supported?**
A: We support `MP3`, `WAV`, `M4A`, `OGG`, and standard `MP4` video files.

**Q: Contact?**
A: security/inquiries: `souravkr529@gmail.com`

---

## 📜 License

This project is licensed under the **MIT License** - feel free to fork, modify, and use it in your own projects.
