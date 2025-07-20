# Task-Management-Parser
# Intelligent Parsing & Structuring of USB Power Delivery (USB PD) Specification Documents

This project is designed to analyze the USB Power Delivery (USB-PD) Specification PDF by extracting its **Table of Contents**, dividing the document into section-based chunks, and enabling you to **query the content** directly from your terminal.


---
## Requirements

- Python 3.8+
- Key libraries:
  - `pdfplumber`
  - `difflib`
  - `json`
  - `os`
  
Install all with:

pip install -r requirements.txt

##  Folder Structure

```
TaskManagementApi-Parser/
├── parser/
│   ├── usb_pd_parser.py           
│   ├── chunk_pdf_by_toc.py        
│   ├── qa_from_chunks.py          
├── pdfs/
│   └── usb-pd-spec.pdf            
├── output/
│   ├── usb_pd_spec.jsonl          
│   └── usb_pd_chunks.jsonl        
├── requirements.txt               
└── README.md                      
```



##  Features

- Extracts structured Table of Contents from technical PDFs
- Splits the PDF into logical section "chunks"
- Lets you ask questions like: `Section 1.2` or `What is USB PD?`
- Returns accurate matching content from the original document

---

##  Setup Instructions

### 1. Clone or unzip the project


cd TaskManagementApi-Parser


### 2. Create virtual environment


python -m venv venv
venv\Scripts\activate      # Windows


### 3. Install dependencies


pip install -r requirements.txt


---

##  How to Use

###  Step 1: Extract Table of Contents


python parser\usb_pd_parser.py


Output: `output/usb_pd_spec.jsonl`


###  Step 2: Chunk the PDF by section


python parser\chunk_pdf_by_toc.py


Output: `output/usb_pd_chunks.jsonl`



###  Step 3: Start QA Terminal


python parser\qa_from_chunks.py


You’ll see:

 Ask a question about the USB PD spec (type 'exit' to quit)
 Your Question:




## Sample Test Case


 Your Question: Section 1.2

 Section: 1.2 Purpose (Score: 1.00)

 Answer:
Compatible with existing spec-compliant USB cables.
Minimizes potential damage from non-compliant cables.
Defines mechanisms to discover, enter and exit Alternate Modes...


You can also ask:

Your Question: What is the purpose of USB Power Delivery?






