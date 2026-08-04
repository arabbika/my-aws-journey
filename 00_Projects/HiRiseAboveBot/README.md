# 🤖 HiRiseAboveBot — WhatsApp AI Tutoring Engine 🤖


---

## 🌍 Community & Educational Impact

HiRiseAboveBot is a live, production WhatsApp-native AI tutoring platform built for Grades 7–12 students following the CAPS and IEB curricula. It provides instant, multi-modal learning assistance—ranging from image OCR problem-solving to automated text-to-speech explanations.

---

## 🏗️ System Architecture

```text
  [ User (WhatsApp) ]
          │
          ▼
   [ Twilio Gateway ]
          │
          ▼
 [ Flask Blueprint Webhook ] ──► [ SQLite User DB / Daily Quota ]
          │
          ├──► [ Tesseract OCR Engine ]  (Image / Handwritten Parsing)
          ├──► [ xAI Grok-4 Model ]       (Step-by-Step CAPS/IEB Solutions)
          └──► [ gTTS Audio Engine ]     (Voice Explanation Generation)
          │
          ▼
   [ LaTeX-to-WhatsApp ] ──► (Formatted Unicode Math Output to User)
```

---

## 🛠️ Tech Stack & Infrastructure

* **Backend Engine:** Python 3, Flask (Blueprint Architecture)
* **AI & Machine Learning:** xAI SDK (`grok-4-fast-reasoning`)
* **Computer Vision / OCR:** Tesseract OCR (`pytesseract`, `Pillow`)
* **Voice & Audio Processing:** Google Text-to-Speech (`gTTS`)
* **Telephony Gateway:** Twilio API for WhatsApp
* **Database & Persistence:** SQLite3
* **Threading:** Asynchronous execution for multi-threaded media handling

---

## 💡 Key Technical Features

* **Multi-Modal Processing:** Handles both raw text prompts and incoming photo submissions via OCR text extraction.
* **WhatsApp Math Rendering:** Custom regex-based parser that converts complex LaTeX syntax (`\frac{}{}`, `\boxed{}`) into readable WhatsApp Unicode formatting.
* **On-Demand Voice Generation:** Dynamically generates short `.mp3` audio lessons delivered straight to the chat.
* **Security & Access Control:** Implements SQLite user verification and daily query limit checks (20 queries/day).

---

## 📸 Platform Interface & Screenshots

| Image OCR Workflow | LaTeX Math Formatting | Voice Explanation |
| :---: | :---: | :---: |
| ![OCR Demo](./screenshots/ocr-demo.png) | ![Math Demo](./screenshots/math-demo.png) | ![Audio Demo](./screenshots/audio-demo.png) |
