📄 Intelligent Document Automation: Smart OCR Bot 🤖

A complete pipeline for automating the extraction of structured information from receipts using OpenCV preprocessing, Tesseract OCR, and Google GenAI.

This project demonstrates Intelligent Document Processing (IDP), which transforms scanned or photographed documents into structured, machine-readable data for easy integration into business workflows.

📋 Table of Contents

Overview

Features

Technologies Used

Installation

Usage

Project Pipeline

Folder Structure

Example Output

Future WorK

📝 Overview

Intelligent Document Processing (IDP) enhances traditional OCR by not only reading text but also understanding its context.

This project focuses on automating the extraction of key information from receipts, including:

🏢 Company Name

📅 Invoice/Receipt Date

📍 Vendor Address

💰 Total Amount

The pipeline includes: image preprocessing, text extraction, and structured data extraction using AI.

✨ Features

⚡ Automated Image Preprocessing: Grayscale conversion, noise reduction, binarization, and deskewing using OpenCV

🔍 OCR Text Extraction: Accurate text recognition using Tesseract

🧠 Structured Data Extraction: Extract key fields (company, date, address, total) using Google GenAI

📂 Batch Processing: Supports multiple receipts at once

💾 JSON Output: Structured results saved as JSON files for easy integration

🛠 Technologies Used

Python 3 🐍

OpenCV (cv2) 🖼️

Pillow (PIL) 🖼️

Tesseract OCR (pytesseract) ✍️

Google Generative AI (genai) 🤖

JSON 📄

Google Colab ☁️ (optional)

⚡ Installation

Clone the repository:

git clone https://github.com/your-username/Intelligent-Document-Automation.git
cd Intelligent-Document-Automation


Install required Python packages:

pip install opencv-python pillow pytesseract


(Optional) For Google Colab integration and GenAI:

pip install google-genai


Install Tesseract OCR on your system:

Ubuntu/Debian:

sudo apt install tesseract-ocr


Windows: Download installer

🚀 Usage

Preprocess Images:

from process_images import process_one_image


Extract Text using Tesseract:

import pytesseract
from PIL import Image

text = pytesseract.image_to_string(Image.open("processed_images/receipt.jpg"))


Extract Structured Data using GenAI:

from google import genai

genai_client = genai.Client(api_key=YOUR_API_KEY)
# Use prompt and Tesseract text to get structured JSON output


Batch Processing:
Run the provided scripts to automatically process multiple images, extract text, and save JSON files.

🛠 Project Pipeline

Image Preprocessing:

Convert to grayscale 🖤

Reduce noise 🧹

Binarize ⚪⚫

Deskew 🔄

OCR Text Extraction:

Use Tesseract OCR to extract text ✍️

Structured Data Extraction:

Feed Tesseract text into GenAI with a custom prompt 🤖

Extract company, date, address, total

Save results as JSON 📄

📂 Folder Structure
Intelligent-Document-Automation/
│
├── processed_images/      # Preprocessed images 🖼️
├── tesseract_output/      # Extracted text from images ✍️
├── json_output/           # Structured JSON results 📄
├── notebooks/             # Colab notebooks ☁️ (optional)
├── process_images.py      # Image preprocessing functions 🛠️
├── extract_text.py        # Tesseract OCR scripts ✍️
├── extract_json.py        # GenAI information extraction scripts 🤖
└── README.md

📊 Example Output
{
    "company": "ABC Retail Pvt Ltd",
    "date": "2025-11-15",
    "address": "123 Main Street, City, Country",
    "total": "₹2,350.00"
}

🔮 Future Work

Support additional document types like invoices, contracts, and forms 📄

Improve OCR accuracy with deep learning-based text recognition 🧠

Export structured data directly to Excel, CSV, or ERP systems 📊

Automate full pipeline on cloud platforms ☁️ for large-scale processing

📜 License
