# AP invoice processing with OCR Agentic AI🤖:

🚀 Project Overview

This project automates the complete AP invoice workflow:

Upload invoice (PDF/Image)

Extract text using OCR

Use AI to understand & structure invoice data

Validate critical fields

Store clean data in a database

Upload invoice to Google Drive

Handle duplicates & errors gracefully

Designed for scalable, real-world finance operations.

🧠 Key Features

✅ Invoice submission form
✅ OCR text extraction from invoices
✅ AI-based invoice data extraction
✅ Structured JSON parsing
✅ Duplicate invoice detection
✅ Database storage (PostgreSQL)
✅ Google Drive upload
✅ End-to-end automated workflow
✅ Production-ready Agentic AI design

🛠️ Tech Stack

n8n – Workflow automation

OCR – Invoice text extraction

OpenAI / LLM – Invoice understanding & structuring

PostgreSQL – Invoice data storage

Google Drive API – File storage

JSON Schema – Data validation

🔄 Workflow Architecture
Step-by-Step Flow

Invoice Submission Form

User uploads invoice (PDF/Image)

Extract Text from Invoice

OCR extracts raw text

Extract Invoice Data with AI

AI reads OCR text

Extracts:

Invoice Number

Vendor Name

Invoice Date

Subtotal

Tax Amount

Total Amount

Currency

Merge Invoice Data

Combine OCR + AI outputs

Parse AI Response to Clean JSON

Convert AI output to structured JSON

Upload Invoice to Google Drive

Store original invoice securely

Invoice Data Store (Database)

Save clean invoice data to PostgreSQL

Prevent duplicate invoices

Store Raw Form Data

Keep raw submission for audit

Success Page

Confirm successful processing
