# AI-Powered Smart Bill Manager 🧾✨

An intelligent mobile application designed to simplify utility bill management and expense tracking. By leveraging the power of **Gemini AI** and **n8n automation**, this app extracts detailed information from uploaded invoice images, visualizes expense trends, and provides clear, AI-driven explanations for price fluctuations between different billing periods.

## 🚀 Features

* **Detailed Invoice Analysis:** Users can upload a photo of their utility bill (electricity, water, gas). The system reads the document and extracts a structured, easy-to-understand breakdown of all costs, taxes, and consumption data.
* **Smart Bill Comparison:** Ever wondered, *"Why is my bill so high this month?"* Upload two different bills, and the AI will compare them to pinpoint the exact reason for the price difference (e.g., increased consumption rate, unit price hikes, or additional taxes).
* **Monthly Expense & Trend Tracking:** Keep all your utility expenses in one place. The app provides visual charts and graphs to track how your spending on each utility changes month by month.

## 🛠️ Architecture & Tech Stack

This project uses a modern, automated pipeline to process complex document data into a user-friendly UI:

* **Frontend:** Kotlin
* **Automation Pipeline:** **n8n** (Node-based Workflow Automation)
* **AI Engine:** **Google Gemini AI**
* **How it works:**
  1. The user uploads an invoice image via the app.
  2. The app triggers an n8n Webhook, sending the image payload.
  3. The n8n workflow connects to the Gemini AI API, prompting it to analyze and extract specific billing data.
  4. Gemini AI returns a structured **JSON** output.
  5. n8n passes the JSON back to the app, which is then parsed and beautifully displayed to the user in seconds.

## ⚙️ Setup & Installation

> ⚠️ **Important Configuration:**
> You need to configure your Webhook URL in `BillsViewModel.kt`:
> ```kotlin
> DEFAULT_WEBHOOK_URL = "https://your-n8n-instance.com/webhook/yourID"
> ```

1. Clone this repository:
   ```bash
   git clone https://github.com/mertdemirci04/FaturamNasil.git
