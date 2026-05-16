# 🧠 AI Exam Evaluator

![Python](https://img.shields.io/badge/Python-3.12-blue?style=flat-square&logo=python&logoColor=white)
![Gradio](https://img.shields.io/badge/Gradio-UI-orange?style=flat-square&logo=gradio&logoColor=white)
![Groq](https://img.shields.io/badge/Groq-Llama%203.3%2070B-black?style=flat-square)
![Llama Vision](https://img.shields.io/badge/Llama-Vision%20OCR-purple?style=flat-square)
![OpenCV](https://img.shields.io/badge/OpenCV-Vision-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

An AI-powered system that automatically reads and evaluates handwritten answer sheets using OCR and Large Language Models — generating structured feedback with marks, grades, and improvement areas instantly.

---

## 🚩 Problem Statement

Evaluating handwritten answer sheets is manual, slow, and inconsistent. Result declaration takes weeks. Students receive only a final mark with zero insight into what went wrong or how to improve.

This project automates that entire pipeline — from reading handwriting to generating detailed, actionable feedback — in seconds.

---

## 🔍 Overview

The AI Exam Evaluator follows a pipeline-based approach:

```
Handwritten Answer Sheet (Image)
        ↓
Image Preprocessing (OpenCV + Pillow)
        ↓
OCR Text Extraction (Llama Vision via Groq API)
        ↓
Question-wise Answer Segmentation
        ↓
AI Grading (Llama 3.3 70B)
        ↓
Structured Feedback Report (Marks + Grade + Insights)
```

---

## ✨ Features

- **Handwriting OCR** — Extracts text from scanned or photographed answer sheets using Llama Vision
- **AI Grading** — Evaluates answers using Llama 3.3 70B with adjustable strictness levels
- **Two Grading Modes** — Auto grading or answer-key-based grading
- **Detailed Feedback** — Per-question marks, strengths, weaknesses, and improvement suggestions
- **Grade Report** — Final score, grade, and structured summary
- **Web Interface** — Clean Gradio UI, no technical knowledge needed to use
- **Faculty-first Design** — Built for college and university use cases

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| OCR & Vision | Llama Vision (Groq API) |
| LLM Grading | Llama 3.3 70B (Groq API) |
| Frontend | Gradio |
| Backend | Python |
| Image Processing | OpenCV, Pillow |
| Deployment | Cloud-based |

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/omermohammedfarooq/ocr-rag-answer-evaluation.git
cd ocr-rag-answer-evaluation
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Set Up Environment Variables

Create a `.env` file in the root directory:

```env
GROQ_API_KEY=your_groq_api_key_here
```

Get your free Groq API key at [console.groq.com](https://console.groq.com)

### 4. Run the App

```bash
python app.py
```

The Gradio interface will launch at `http://localhost:7860`

---

## 🎯 End Users

- **Faculty & Professors** — Automate evaluation, save hours per exam cycle
- **Colleges & Universities** — Scale grading without scaling effort
- **Coaching Institutes** — Fast feedback for practice tests
- **EdTech Platforms** — Integrate AI evaluation into existing workflows
- **Students** — Understand exactly where marks were lost

---

## 📁 Project Structure

```
ocr-rag-answer-evaluation/
├── app.py                  # Main Gradio app
├── ocr.py                  # Llama Vision OCR pipeline
├── evaluator.py            # LLM grading logic
├── feedback.py             # Feedback report generation
├── requirements.txt
├── .env.example
└── README.md
```

---

## 🔮 Future Improvements

- [ ] Support for multi-page answer sheets
- [ ] PDF upload support
- [ ] Batch evaluation (multiple students at once)
- [ ] Custom rubric / marking scheme upload
- [ ] Student dashboard with historical feedback
- [ ] Export reports as PDF
- [ ] Integration with college ERP systems

---

## 👨‍💻 Author

**Mohammed Omer Farooq**
- GitHub: [@omermohammedfarooq](https://github.com/omermohammedfarooq)
- LinkedIn: [Mohammed Omer Farooq](https://linkedin.com/in/omermohammedfarooq)
- Email: omermohammedfarooq@gmail.com

---

## 🙏 Acknowledgments

- [Groq](https://groq.com) — Ultra-fast LLM inference API
- [Meta AI](https://ai.meta.com) — Llama Vision and Llama 3.3 70B models
- [Gradio](https://gradio.app) — Web UI framework

---

## 📝 License

MIT License — see [LICENSE](LICENSE) for details.

---

**Built to make feedback faster, fairer, and actually useful.**
