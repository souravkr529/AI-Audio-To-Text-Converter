<div align="center">

# 🎙️ DuoAI: Audio To Text Converter

### 🔒 Secure • ⚡ Fast • 🧠 Dual AI • 📱 Mobile Ready

[![License](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)
[![Privacy](https://img.shields.io/badge/Privacy-Local_Only-green.svg?style=for-the-badge)](SECURITY.md)
[![Gemini](https://img.shields.io/badge/AI-Gemini_2.0-blueviolet.svg?style=for-the-badge&logo=google)](https://aistudio.google.com/)
[![OpenAI](https://img.shields.io/badge/AI-GPT--4o-10a37f.svg?style=for-the-badge&logo=openai)](https://openai.com/)
[![Platform](https://img.shields.io/badge/Platform-PWA%20Ready-orange?style=for-the-badge&logo=googlechrome)](https://souravkr529.github.io/AI-Audio-To-Text-Converter/)

**A next-generation automated transcription tool designed for absolute privacy and speed.**
<br>
Runs entirely in your browser using **Google Gemini** or **OpenAI** directly.

[Live Demo](https://souravkr529.github.io/AI-Audio-To-Text-Converter/) •
[Features](#-key-features) •
[Installation](#-installation) •
[Security](#-security-architecture) •
[Support](#-support)

---

</div>

## 🎯 What is DuoAI?

**DuoAI Audio To Text** is a secure, serverless web application that converts audio files into professional text transcripts. Unlike traditional services that upload your sensitive recordings to a third-party server, DuoAI functions entirely within **your browser**. 

It establishes a direct, encrypted connection to **Google's Gemini 2.0 Flash** or **OpenAI's GPT-4o** using your personal API key. This means faster processing, lower costs, and guaranteed data privacy.

---

## ✨ Key Features

*   **🤖 Dual AI Engine**: Switch seamlessly between **Google Gemini** (Free Tier available) and **OpenAI** models.
*   **💬 Smart Conversational UI**: 
    *   **Auto-Speaker Detection**: Identifies different speakers uniquely.
    *   **WhatsApp-Style Interface**: Renders transcripts as a readable chat thread with distinct colors.
*   **📄 Document Mode**: Automatically formats single-speaker audio into clean, readable articles or notes.
*   **⚡ Zero Latency Architecture**: Bypasses backend processing completely. Audio streams directly from Client ➔ AI Provider.
*   **🌍 Universal Translation**: Auto-detects and transcribes mixed-language audio (e.g., Hinglish, Spanglish) with high accuracy.
*   **📱 Mobile Optimized**: A fully responsive Progressive Web App (PWA) feel on iOS and Android.

---

## 🌊 How It Works (Workflow)

We utilize a **Bring Your Own Key (BYOK)** architecture for maximum security and flexibility.

```mermaid
graph TD
    User([👤 User])
    Browser[("💻 Web Browser")]
    AI_Service[("🧠 AI Cloud (Google/OpenAI)")]
    
    subgraph Local_Device ["🔒 Your Device (Safe Zone)"]
        User -- "1. Enters API Key" --> Browser
        User -- "2. Selects Audio File" --> Browser
        Browser -- "3. Validates Key & File" --> Browser
    end
    
    Browser == "4. Sends Encrypted Audio (Direct)" ==> AI_Service
    AI_Service -- "5. Returns JSON Transcript" ==> Browser
    
    Browser -- "6. Renders Chat/Document UI" --> User
```

---

## 🔒 Security Architecture

DuoAI represents the gold standard for privacy-conscious tools:

### 🛡️ The "Zero-Server" Guarantee
1.  **No Database**: We do not store your name, email, audio, or transcripts.
2.  **No Middleman**: There is no backend server intercepting your data.
3.  **Local Encryption**: Key credentials are stored in `localStorage` and never transmit to us.

---

## 🚀 Quick Start Guide

### Step 1: Get Your Free API Key
*   **Google Gemini**: [Get Free Key Here](https://aistudio.google.com/app/apikey) (Recommended for free usage)
*   **OpenAI**: [Get Key Here](https://platform.openai.com/api-keys)

### Step 2: Start Transcribing
1.  Open the [Live Tool](https://souravkr529.github.io/AI-Audio-To-Text-Converter/).
2.  Select your preferred AI Provider (Gemini or OpenAI).
3.  Paste your API Key (it saves automatically).
4.  Drop your audio file (`MP3`, `M4A`, `WAV`).
5.  **Done!** Download your transcript as a text file.

---

## 📦 Installation (Local Development)

To run this project on your local machine:

```bash
# 1. Clone the repository
git clone https://github.com/souravkr529/AI-Audio-To-Text-Converter.git

# 2. Navigate to the project folder
cd AI-Audio-To-Text-Converter

# 3. Launch
# Simply open 'index.html' in Chrome or Edge.
# No node_modules or server setup required!
```

---

## 🛠️ Technical Stack

*   **Core**: HTML5, Vanilla JavaScript (ES6 Modules)
*   **Styling**: TailwindCSS (CDN for lightweight loading)
*   **AI Integration**: RESTful API integration with Gemini 1.5/2.0 and GPT-4o
*   **Security**: Strict Content Security Policy (CSP), Sanitized Inputs

---

## 🙋‍♀️ FAQ

**Q: Is this tool really free?**
<br>
A: **Yes.** The tool itself is free and open-source. You only use your own API calls (Gemini offers a generous free tier).

**Q: Can you see my API Key?**
<br>
A: **Never.** Your key stays in your browser. If you clear your history, it's gone.

**Q: Does it support long audio?**
<br>
A: **Yes.** Tested with files up to 1-2 hours (dependent on model limits).

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## 📞 Support

- 🐛 [Report Bug](https://github.com/souravkr529/AI-Audio-To-Text-Converter/issues)
- 💡 [Request Feature](https://github.com/souravkr529/AI-Audio-To-Text-Converter/issues)
- ⭐ **Star this repo if you find it useful!**

---

<div align="center">

**Made with ❤️ by [Sourav Kumar](https://github.com/souravkr529)**

</div>
