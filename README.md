# 🧾 Receipt Guru AI

> **From phone snapshot to trustworthy expense intelligence.**

Smart Receipt & Invoice Snapshot Auditor is an AI-powered expense analysis web application that transforms receipt and invoice images into structured, reviewable financial data.

Instead of manually entering receipt information into spreadsheets, users can upload a receipt image and extract important details such as amount, date, store name, and tax information. The system then categorizes expenses and highlights potential duplicate or unusually high transactions.

---

## 🚀 Problem

For freelancers and small businesses, managing receipts manually can become a repetitive and time-consuming process.

A typical workflow involves:

1. 📸 Capturing the receipt
2. 🔍 Reading the receipt details
3. ⌨️ Manually entering the information
4. 🗂️ Categorizing the expense
5. 🔎 Checking for duplicates or unusual charges

This repetitive process increases the possibility of human error and makes it easier for suspicious or duplicate transactions to go unnoticed.

---

## 💡 Our Solution

**Smart Receipt & Invoice Snapshot Auditor** turns a single receipt image into structured expense intelligence.

### Core Workflow

```text
Receipt Image
      ↓
     OCR
      ↓
Field Extraction
      ↓
Expense Categorization
      ↓
Duplicate / Anomaly Detection
      ↓
Financial Dashboard
```

**Upload → Extract → Classify → Analyze → Visualize**

---

## ✨ Key Features

### 📷 Instant OCR & Image Parsing

Upload a receipt or invoice image and automatically extract important information.

**Extracted fields include:**

- 💰 Total Amount
- 📅 Date
- 🏪 Store / Merchant Name
- 🧾 Tax Details

The application uses **Gemini Vision API** and **Tesseract.js** for image and text extraction.

### 🗂️ Automatic Expense Categorization

Expenses are automatically categorized to make financial analysis easier.

Example categories:

- 🍔 Food
- ✈️ Travel
- 📦 Supplies
- And other expense categories

### ♻️ Duplicate Detection

The system identifies potentially repeated receipts and can help users catch:

- The same receipt being uploaded multiple times
- Duplicate expense entries
- Repeated transactions requiring review

### 🚨 Anomaly Detection

The application highlights unusually high or suspicious charges so users can focus their attention on transactions that require investigation.

### 📊 Financial Dashboard

Extracted expenses are presented through a visual dashboard containing:

- Expense breakdown
- Category distribution
- Transaction overview
- Review signals
- Anomaly indicators

Charts and visualizations are powered by **Chart.js**.

---

## 🏗️ Architecture

```text
                    ┌───────────────────┐
                    │   Receipt Image   │
                    └─────────┬─────────┘
                              │
                              ▼
                  ┌───────────────────────┐
                  │   OCR / AI Extraction │
                  │                       │
                  │ Gemini Vision API     │
                  │ Tesseract.js          │
                  └───────────┬───────────┘
                              │
                              ▼
                  ┌───────────────────────┐
                  │   Structured Data     │
                  │                       │
                  │ Amount                │
                  │ Date                  │
                  │ Store Name            │
                  │ Tax Details           │
                  └───────────┬───────────┘
                              │
                 ┌────────────┴────────────┐
                 ▼                         ▼
        ┌─────────────────┐       ┌─────────────────┐
        │ Categorization  │       │ Anomaly /       │
        │                 │       │ Duplicate Check │
        └────────┬────────┘       └────────┬────────┘
                 │                         │
                 └────────────┬────────────┘
                              ▼
                  ┌───────────────────────┐
                  │   Financial Dashboard │
                  │                       │
                  │ React + Tailwind CSS  │
                  │ Chart.js              │
                  └───────────────────────┘
```

---

## 🛠️ Tech Stack

<p align="center">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" width="55" alt="React"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" width="55" alt="JavaScript"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-original.svg" width="55" alt="Tailwind CSS"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" width="55" alt="HTML5"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" width="55" alt="CSS3"/>
</p>

<p align="center">
  <strong>React</strong> • <strong>JavaScript</strong> • <strong>Tailwind CSS</strong> • <strong>HTML5</strong> • <strong>CSS3</strong>
</p>

### AI & Data Processing

<p align="center">
  <img src="https://cdn.simpleicons.org/googlegemini/8E75B2" width="55" alt="Google Gemini"/>
  <img src="https://cdn.simpleicons.org/tesseract/5A5A5A" width="55" alt="Tesseract"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/chartjs/chartjs-original.svg" width="55" alt="Chart.js"/>
</p>

<p align="center">
  <strong>Gemini Vision API</strong> • <strong>Tesseract.js</strong> • <strong>Chart.js</strong>
</p>

| Technology | Purpose |
|---|---|
| ⚛️ React | Frontend application |
| 🎨 Tailwind CSS | UI styling |
| 🤖 Gemini Vision API | AI-powered receipt/image understanding |
| 🔎 Tesseract.js | OCR / text extraction |
| 📊 Chart.js | Financial data visualization |
| 🌐 HTML / CSS / JavaScript | Web application foundation |

---

## 🔄 How It Works

### 1. Upload

The user uploads a photo of a receipt or invoice.

### 2. Extract

The image is processed using OCR and AI-powered image understanding.

```text
Amount
Date
Store Name
Tax Details
```

### 3. Classify

The extracted transaction is automatically assigned an expense category such as:

```text
Food
Travel
Supplies
```

### 4. Analyze

The application checks the transaction for:

```text
Duplicate Receipt
        +
Unusual / High Charge
```

### 5. Visualize

The processed information is displayed through an interactive financial dashboard.

---

## 📊 Example

### Input

```text
┌─────────────────────────┐
│        RECEIPT          │
│                         │
│ ABC SUPERMARKET         │
│ 07/10/2026              │
│                         │
│ Subtotal     ₹850       │
│ Tax           ₹42.50    │
│ TOTAL        ₹892.50    │
│                         │
└─────────────────────────┘
```

### Extracted Data

```json
{
  "merchant": "ABC SUPERMARKET",
  "date": "07/10/2026",
  "amount": 892.50,
  "tax": 42.50,
  "category": "Food"
}
```

---

## 📁 Project Structure

```text
smart-receipt-auditor/
│
├── public/
│   └── ...
│
├── src/
│   ├── components/
│   │   ├── Dashboard/
│   │   ├── ReceiptUploader/
│   │   ├── ExpenseTable/
│   │   ├── Charts/
│   │   └── AnomalyAlert/
│   │
│   ├── services/
│   │   ├── gemini.js
│   │   └── ocr.js
│   │
│   ├── utils/
│   │   ├── categorization.js
│   │   └── anomalyDetection.js
│   │
│   ├── App.jsx
│   └── main.jsx
│
├── .env
├── package.json
├── tailwind.config.js
└── README.md
```

> Adjust the structure according to the actual implementation in your repository.

---

## ⚙️ Getting Started

### Prerequisites

- Node.js
- npm
- Gemini API key

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/smart-receipt-auditor.git
cd smart-receipt-auditor
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

Create a `.env` file:

```env
GEMINI_API_KEY=your_api_key_here
```

> ⚠️ Never commit API keys or other secrets to GitHub.

### 4. Start the development server

```bash
npm run dev
```

Open the local development URL shown in your terminal.

---

## 🎯 Impact

### ⏱️ Saves Time

Reduces repetitive manual receipt data-entry work.

### 👁️ Improves Visibility

Transforms scattered receipts into structured expense information.

### 🗂️ Consistent Categorization

Automatically organizes transactions into useful expense categories.

### 🚨 Finds Risk

Potentially suspicious, duplicate, or unusually high transactions are surfaced for review.

---

## 🔮 Future Scope

The project can be extended with:

- 🔗 Accounting software integrations
- 🌍 Multi-language receipt support
- 🧠 Smarter anomaly detection
- 🔔 Budget alerts
- 👥 Multi-user expense management
- 📈 Advanced financial analytics
- ☁️ Cloud-based expense history
- 📱 Dedicated mobile application

---

## 🏆 Hackathon

### CYRUS HACK-A-THON — CHH 2026

**Problem Statement:** Smart Receipt & Invoice Snapshot Auditor

**Track:** FinTech & Vision Automation

**Theme:** Practical Impact

---

## 👥 Team — TECH TITANS

| Member | Role |
|---|---|
| **Md Alfaz** | Team Leader |
| **Sonakshi Upadhyay** | Team Member |
| **Divyanshu Kumar** | Team Member |
| **Utkarsh Singh** | Team Member |

---

## 🧠 Project Philosophy

```text
SNAPSHOT
   ↓
STRUCTURE
   ↓
SIGNAL
   ↓
ACTION
```

Turn an ordinary receipt snapshot into structured financial information, surface important signals, and help users make faster decisions.

---

## 📜 License

This project was developed as part of **CYRUS HACK-A-THON (CHH 2026)**.

Add your preferred license here, for example:

```text
MIT License
```

---

## ⭐ Support

If you like this project, consider giving the repository a ⭐.

Built with ❤️ by **Team TECH TITANS** for **CYRUS HACK-A-THON 2026**.
# 🧾 Receipt Guru AI
