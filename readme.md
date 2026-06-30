# 🤖 WhatsApp AI Order Management Bot

An AI-powered **WhatsApp chatbot** built using **n8n**, **Google Gemini**, **Google Sheets**, and the **WhatsApp Cloud API**. The bot intelligently responds to customer queries, checks product availability, answers FAQs, and records customer orders automatically—all without any manual intervention.

---

## 📸 Workflow

![Workflow](./Screenshot%202026-06-30%20160241.png)

> **⚠️ Note**
>
> The **red warning icons** on the WhatsApp nodes are **intentional**. They appear because the **WhatsApp Cloud API credentials have been removed** before publishing this repository for **privacy and security reasons**. Once valid credentials are configured, the workflow functions normally.

---

# ✨ Features

- 🤖 AI-powered conversations using **Google Gemini**
- 📦 Real-time inventory lookup from Google Sheets
- ❓ Answers customer FAQs automatically
- 🛒 Stores customer orders directly into Google Sheets
- 🧠 Context-aware conversations using memory
- 📱 WhatsApp Cloud API integration
- ⚡ Fully automated n8n workflow
- 📊 Easy to customize by editing Google Sheets
- 🔄 No coding required for updating products or FAQs
- 🚀 Scalable for small businesses and restaurants

---

# 🏗️ Workflow Architecture

```text
                Customer
                   │
                   ▼
         WhatsApp Cloud API
                   │
                   ▼
          WhatsApp Trigger
                   │
                   ▼
             AI Agent (Gemini)
                   │
        ┌──────────┼──────────┐
        │          │          │
        ▼          ▼          ▼
 Inventory     FAQ Sheet   Orders Sheet
 (Read)         (Read)      (Append)
        │
        ▼
     AI Response
        │
        ▼
 Send WhatsApp Message
```

---

# 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| **n8n** | Workflow Automation |
| **Google Gemini API** | AI Conversations |
| **WhatsApp Cloud API** | Messaging Platform |
| **Google Sheets** | Inventory, FAQs & Order Storage |

---

# 📂 Google Sheets Structure

The project uses a single Google Spreadsheet containing three sheets.

| Sheet | Description |
|--------|-------------|
| 📦 **Inventory** | Stores products, prices, stock availability and related information |
| ❓ **FAQ** | Stores frequently asked questions and predefined answers |
| 🛒 **Orders** | Automatically records every customer order |

### Google Sheets Template

https://docs.google.com/spreadsheets/d/1QqzaApnP_WWV8403H8KFLuh7m2My6s1ENKBuaHfdkKs/edit?usp=sharing

---

# 🔄 How It Works

1. A customer sends a message on WhatsApp.
2. The **WhatsApp Trigger** starts the workflow.
3. The message is forwarded to the **Google Gemini AI Agent**.
4. Based on the customer's request, the AI:
   - Reads product details from the **Inventory** sheet.
   - Searches answers in the **FAQ** sheet.
   - Saves confirmed orders to the **Orders** sheet.
5. Gemini generates a natural language response.
6. The reply is automatically sent back to the customer via WhatsApp.

---

# 🚀 Example Use Cases

- 🛒 Grocery Stores
- 🍕 Restaurants
- ☕ Cafés
- 🏪 Retail Shops
- 📦 Inventory Management
- 💬 Customer Support
- 📋 Order Management
- 🛍️ Small Businesses

---

# 📁 Repository Structure

```text
.
├── workflow.json
├── Screenshot 2026-06-30 160241.png
├── README.md
└── Google Sheets Template
```

---

# 🔒 Privacy & Security

For security reasons, this repository **does not include**:

- WhatsApp Cloud API Credentials
- Google Gemini API Key
- Google OAuth Credentials
- Personal Authentication Tokens
- Environment Variables

You will need to configure your own credentials before running the workflow.

---

# 📦 Setup Guide

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/your-repository.git
```

---

### 2. Import the Workflow

Import `workflow.json` into your n8n instance.

---

### 3. Configure Credentials

Configure the following credentials inside n8n:

- Google Gemini API
- Google Sheets OAuth
- WhatsApp Cloud API

---

### 4. Create Google Sheets

Create a Google Spreadsheet using the provided template with the following sheets:

- Inventory
- FAQ
- Orders

---

### 5. Activate Workflow

Enable the workflow and start chatting with your WhatsApp bot.

---

# 💡 Customization

You can easily customize the chatbot by editing the Google Sheets:

- Add or remove products
- Update prices
- Modify FAQs
- Add more AI tools
- Extend the workflow with payment gateways or databases

No code changes are required.

---

# 📈 Future Improvements

- 💳 Payment Gateway Integration
- 📍 Live Order Tracking
- 🖼️ Image Recognition
- 🌐 Multi-language Support
- 📊 Dashboard & Analytics
- 🧾 Invoice Generation
- 📦 Database Integration
- 🔔 Admin Notifications

---

# 🤝 Contributing

Contributions are welcome!

Feel free to fork the repository, improve the workflow, and submit a pull request.

---

## ⭐ Support

If you found this project helpful, please consider giving it a **⭐ Star** on GitHub.

It helps others discover the project and motivates further development.
