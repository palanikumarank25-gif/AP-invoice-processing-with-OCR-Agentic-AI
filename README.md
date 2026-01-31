# AP Invoice Processing with OCR Agentic AI 🤖

An end-to-end **Accounts Payable (AP) Invoice Processing system** built using **n8n**, **OCR**, and **Agentic AI** to automatically extract, validate, and store invoice data with minimal human intervention.

---

## 🚀 Project Overview

This project automates the complete AP invoice workflow:

- Upload invoice (PDF/Image)
- Extract text using OCR
- Use AI to understand & structure invoice data
- Validate critical fields
- Store clean data in a database
- Upload invoice to Google Drive
- Handle duplicates & errors gracefully

Designed for **scalable, real-world finance operations**.

---

## 🧠 Key Features

- Invoice submission form  
- OCR text extraction from invoices  
- AI-based invoice data extraction  
- Structured JSON parsing  
- Duplicate invoice detection  
- Database storage (PostgreSQL)  
- Google Drive upload  
- End-to-end automated workflow  
- Production-ready Agentic AI design  

---

## 🛠️ Tech Stack

- **n8n** – Workflow automation  
- **OCR** – Invoice text extraction  
- **OpenAI / LLM** – Invoice understanding & structuring  
- **PostgreSQL** – Invoice data storage  
- **Google Drive API** – File storage  
- **JSON Schema** – Data validation  

---

## 🔄 Workflow Architecture

### Step-by-Step Flow

1. **Invoice Submission Form**  
   User uploads invoice (PDF/Image)

2. **Extract Text from Invoice**  
   OCR extracts raw text

3. **Extract Invoice Data with AI**  
   AI extracts:
   - Invoice Number  
   - Vendor Name  
   - Invoice Date  
   - Subtotal  
   - Tax Amount  
   - Total Amount  
   - Currency  

4. **Merge Invoice Data**  
   Combine OCR + AI outputs

5. **Parse AI Response to Clean JSON**  
   Convert AI output to structured JSON

6. **Upload Invoice to Google Drive**  
   Store original invoice securely

7. **Invoice Data Store (Database)**  
   Save clean invoice data to PostgreSQL  
   Prevent duplicate invoices

8. **Store Raw Form Data**  
   Keep raw submission for audit

9. **Success Page**  
   Confirm successful processing

--- 

⚙️ How to Use

Import the workflow JSON into n8n

Configure:
OpenAI credentials
PostgreSQL credentials
Google Drive credentials
Activate the workflow
Upload an invoice
Automation runs end-to-end 

--- 

## 🗄️ Database Schema (PostgreSQL)

```sql
CREATE TABLE invoices (
  invoiceNumber VARCHAR(50) PRIMARY KEY,
  vendorName VARCHAR(255),
  invoiceDate DATE,
  subtotal NUMERIC,
  taxAmount NUMERIC,
  totalAmount NUMERIC,
  currency VARCHAR(10),
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

---






