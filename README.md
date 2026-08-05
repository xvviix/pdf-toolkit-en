<div align="center">

<br/>

# 📄 PDF Toolkit v12

### Powerful PDF Tool — English Version

<br/>

> A complete, standalone PDF utility: split, merge, convert, rotate,
> compress and extract text — plus **automatic name detection with OCR**
> for scanned documents such as certificates and official records.

<br/>

<img src="https://img.shields.io/badge/Python-3.8%2B-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"/>
<img src="https://img.shields.io/badge/OCR-PaddleOCR-4F46E5?style=flat-square" alt="OCR"/>
<img src="https://img.shields.io/badge/UI-Tkinter-10B981?style=flat-square" alt="UI"/>
<img src="https://img.shields.io/badge/Windows-✓-06B6D4?style=flat-square" alt="Windows"/>
<img src="https://img.shields.io/badge/Linux-✓-06B6D4?style=flat-square" alt="Linux"/>

</div>

---

## ✨ Features

| Section | Description |
|---------|-------------|
| ✂️ **Split / Extract** | Split all pages, extract selected pages, or every N pages into one file |
| 🔗 **Merge** | Combine multiple PDFs into one with custom order |
| 🖼️ **PDF to Images** | Convert pages to PNG / JPEG / WEBP with custom DPI |
| 📸 **Images to PDF** | Create a PDF from multiple images |
| 🛠️ **Advanced Tools** | Rotate pages, compress PDF, extract text to TXT |
| 🤖 **Auto Name Detection (OCR)** | Read "first name / last name" from scanned documents and use as file name |
| 💛 **Yellow Highlight** | If a page has multiple names, only the highlighted one is read |
| ✅ **Name Validation** | Score and warn about suspicious extracted names |
| 📊 **Final Report** | Operation summary + output file integrity check |

## 🚀 Quick Start

**On Windows — just double-click `run.bat`.**

This script automatically:
1. Checks that Python is installed
2. Installs required libraries (first run only)
3. Launches the program

**On Linux / macOS:**

```bash
pip install -r requirements.txt
python pdf_toolkit_v12.py
```

## 🖥️ Prerequisites

- Python 3.8 to 3.12 (3.12 recommended)
- Internet connection on first run (to download OCR models)

## 💡 Tip: when a page has multiple names

If one page of the PDF has several "first name / last name" entries:

1. Open the PDF in Adobe Acrobat, Microsoft Edge or any PDF viewer
2. Use the **Highlight** tool to highlight the wanted name **in yellow**
3. Save the file (Ctrl+S)
4. The program only uses the highlighted name for the file name

> If there is no highlight, the program reads the whole page.

## 📁 Project Structure

```
pdf-toolkit-en/
├── run.bat               ← Windows launcher (double-click)
├── pdf_toolkit_v12.py    ← Main program
├── requirements.txt      ← Dependencies
├── README.md             ← This file
└── icon_for_exe.ico      ← Icon (optional)
```

## 📦 Manual Install (if needed)

```bash
pip install -r requirements.txt
```

## 🛠️ Troubleshooting

| Problem | Solution |
|---------|----------|
| Program doesn't open | Run `run.bat` again to see the error message |
| Auto detection doesn't work | Check your internet connection and run again |
| Python 3.13 installed | Install Python 3.12 (3.13 is incompatible with OCR) |

---

<div align="center">

**Made with ❤️ — zero runtime dependencies**

</div>
