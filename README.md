<div align="center">

<br/>

# 📄 PDF Toolkit v12

### The Complete PDF Tool — English Version

<br/>

> A **standalone, zero-runtime-dependency** PDF utility:
> split, merge, convert to images, rotate, compress and extract text —
> plus **automatic name detection with OCR** for scanned documents
> such as certificates, ID cards and official forms.

<br/>

<img src="https://img.shields.io/badge/Python-3.8%2B-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"/>
<img src="https://img.shields.io/badge/Version-v12-10B981?style=flat-square" alt="Version"/>
<img src="https://img.shields.io/badge/OCR-PaddleOCR-4F46E5?style=flat-square" alt="OCR"/>
<img src="https://img.shields.io/badge/UI-Tkinter-10B981?style=flat-square" alt="UI"/>
<img src="https://img.shields.io/badge/Windows-✓-06B6D4?style=flat-square&logo=windows&logoColor=white" alt="Windows"/>
<img src="https://img.shields.io/badge/Linux-✓-06B6D4?style=flat-square&logo=linux&logoColor=white" alt="Linux"/>
<img src="https://img.shields.io/badge/macOS-✓-06B6D4?style=flat-square&logo=apple&logoColor=white" alt="macOS"/>
<img src="https://img.shields.io/badge/License-MIT-green?style=flat-square" alt="MIT"/>
<img src="https://github.com/xvviix/pdf-toolkit-en/actions/workflows/ci.yml/badge.svg" alt="CI"/>

<br/>

**[🚀 Quick Start](#-quick-start)** •
**[✨ Features](#-features)** •
**[🤖 Auto Name Detection](#-auto-name-detection-ocr)** •
**[📖 Usage Guide](#-usage-guide)** •
**[🛠️ Troubleshooting](#️-troubleshooting)**

</div>

---

## 🖼️ App Preview

```
┌──────────────────────────────────────────────────────────────┐
│  📄  PDF Toolkit v12        — Powerful PDF Tool              │
├──────────────────────────────────────────────────────────────┤
│  📁 Input PDF Files          [＋ Add PDF] [📁 Add Folder]      │
│  ┌────────────────────────────────────────────────────────┐  │
│  │  document1.pdf                                         │  │
│  │  document2.pdf                                         │  │
│  └────────────────────────────────────────────────────────┘  │
│  📂 Output Folder:  [C:\Users\...\PDF_Toolkit_Output] [Browse]│
│                                                              │
│  [✂ Split/Extract] [🔗 Merge] [🖼 PDF→Images] [📸 Images→PDF] │
│  [🛠 Advanced Tools]                                          │
│                                                              │
│  ████████████████████░░░░░░░  Progress                       │
│  [▶ Run]  [ℹ Info]  [Clear List]                            │
└──────────────────────────────────────────────────────────────┘
```

---

## ✨ Features

### 📑 Core Operations

| Section | Features |
|---------|----------|
| ✂️ **Split / Extract** | Three modes: split all pages into separate files • extract selected pages • every N pages into one file |
| 🔗 **Merge** | Combine multiple PDFs into one, reorder with ↑↓ buttons |
| 🖼️ **PDF to Images** | Convert pages to PNG / JPEG / WEBP with adjustable quality (72–600 DPI) |
| 📸 **Images to PDF** | Create a PDF from multiple images (order preserved) |
| 🛠️ **Advanced Tools** | Rotate pages (90/180/270/-90) • compress • extract text to TXT |

### 🤖 Auto Name Detection (OCR)

| Feature | Description |
|---------|-------------|
| **Read person names** | First + last name read from scanned documents and used as the **file name** |
| **Persian + English** | Automatic detection for both languages (Persian models pre-bundled) |
| **💛 Yellow Highlight** | If a page has multiple names, only the highlighted area (in yellow) is read |
| **👁 Preview** | See which names were detected before running — no files created |
| **✅ Validation** | Every name gets a 0–100 score; suspicious names marked ⚠, broken ones ✗ |
| **🔢 Duplicate names** | If two people share a name, "name 2", "name 3"... are added automatically |

### 📊 Reporting & Safety

- **Final report** after every operation: file count, total pages, per-file integrity
- **Integrity check** — output files are re-opened to confirm they were built correctly
- **Real progress bar** — exact percentage during long operations
- **Safe file names** — invalid characters (`\ / : * ? " < > |`) are removed automatically

---

## 🚀 Quick Start

### 🪟 Windows — the easy way

Just **double-click `run.bat`**. It automatically:

1. ✅ Checks that Python is installed (shows guidance if not)
2. ✅ Installs the light core libraries (first run only)
3. ✅ Asks if you want OCR (~1GB, optional)
4. ✅ Launches the program

### 🐧 Linux / macOS

```bash
# 1. Install core dependencies (light)
pip install -r requirements.txt

# 2. Optional — OCR for "Automatic (OCR)" name detection (~1GB)
pip install -r requirements-ocr.txt

# 3. Run the program
python pdf_toolkit_v12.py
```

### 📦 Manual Install (optional)

```bash
# With a virtual environment (recommended)
python -m venv venv
source venv/bin/activate    # Linux/macOS
venv\Scripts\activate       # Windows
pip install -r requirements.txt        # core only
pip install -r requirements-ocr.txt    # optional OCR (~1GB)

# Run
python pdf_toolkit_v12.py
```

---

## 🖥️ Prerequisites

| Requirement | Description |
|-------------|-------------|
| **Python** | **3.10 – 3.13** — **3.12 recommended** |
| **Internet** | Only on first run (to install libraries) — OCR models are pre-bundled |
| **OS** | Windows 10/11, Linux or macOS |

> ⚠️ **Python 3.14+ is NOT supported yet** — `paddlepaddle` (the OCR engine) has no wheels for it and the install will fail. Use Python 3.12 or 3.13.

> 💡 **OCR is optional.** The core app (split, merge, convert, naming manually) needs only the light `requirements.txt`. The ~1GB OCR stack is installed separately for the "Automatic (OCR)" name detection only.

---

## 🤖 Auto Name Detection (OCR)

### How it works

```
Scanned PDF (certificate, form, ID)
        │
        ▼
[1] Each page is converted to an image
        │
        ▼
[2] The OCR engine reads the text
        │
        ▼
[3] "First name" and "Last name" are located
        │
        ▼
[4] File name = full person name
  "Sohrab Zarei.pdf"
```

### Real-world example

A death certificate with "Name: Sohrab" and "Family: Zarei" fields:

```
📄 Sohrab Zarei.pdf
📄 Somenbar Keshavarzi.pdf
📄 Marzieh Zarenejad.pdf
📄 Mehdi Zarrinkhoo.pdf
```

### 💡 When a page has multiple names

1. Open the PDF in Adobe Acrobat, Microsoft Edge or any PDF viewer
2. Use the **Highlight** tool to highlight the wanted name **in yellow**
3. Save the file (Ctrl+S)
4. The program only reads the highlighted area

> If there is no highlight, the program reads the whole page.

### 👁 Preview before running

Press the "Preview Names" button to see what the OCR detected:

```
✓ document.pdf • Page 1  ←  Sohrab Zarei (100%)
⚠ document.pdf • Page 2  ←  Sohrab Zarei; (70%) — punctuation: ;
✗ document.pdf • Page 3  ←  (not detected)
```

---

## 📖 Usage Guide

### Step 1 — Add files

- **＋ Add PDF** — pick multiple files
- **📁 Add Folder** — load all PDFs from a folder
- Files appear in the list

### Step 2 — Choose an operation

| Tab | What it does |
|-----|--------------|
| ✂️ Split/Extract | Split mode + page range (e.g. `1-5,8`) + naming type |
| 🔗 Merge | Reorder files with ↑↓ + output file name |
| 🖼️ PDF to Images | DPI, format (PNG/JPEG/WEBP) and page range |
| 📸 Images to PDF | Add images + output file name |
| 🛠 Advanced Tools | Rotation angle, compression quality, text-extraction range |

### Step 3 — Output naming

| Mode | Description |
|------|-------------|
| **Manual (pattern)** | e.g. `{name}_p{page}` → `document_p1.pdf` |
| **Automatic (OCR)** | Person's name read from the document → `Sohrab Zarei.pdf` |

### Step 4 — Run

Press **"▶ Run Operation"**. When finished, the **final report** is shown.

---

## 📁 Project Structure

```
pdf-toolkit-en/
├── run.bat               ← Windows launcher (double-click)
├── pdf_toolkit_v12.py    ← Main program (full source)
├── requirements.txt      ← Dependencies
├── README.md             ← This file
├── LICENSE               ← MIT license
├── test_smoke.py         ← Automated tests
├── .gitignore            ← Ignored files
└── .paddlex/             ← OCR models (pre-bundled — no internet needed)
    └── official_models/
        ├── PP-OCRv5_mobile_det/        ← Text detection model
        └── arabic_PP-OCRv5_mobile_rec/ ← Persian/Arabic reading model
```

---

## 🛠️ Troubleshooting

| Problem | Solution |
|---------|----------|
| Program doesn't open | Run `run.bat` again to see the error message |
| "Python not found" error | Install Python 3.10–3.13 from python.org and check "Add to PATH" |
| Install fails on Python 3.14 | `paddlepaddle` has no 3.14 wheels yet — install Python 3.12 or 3.13 |
| Auto detection doesn't work | Make sure you installed `requirements-ocr.txt` (OCR is optional) |
| Auto detection fails to install | OCR stack is ~1GB — check disk space and internet, or use Python 3.12/3.13 |
| Names are garbled | Scan the page better, or highlight the wanted name in yellow |
| Library install failed | Check your internet connection and run `run.bat` again |
| Output file won't open | Check the final report — if not "valid", re-run the operation |

---

## ❓ FAQ

**Q: Is internet needed for the OCR models?**
No — the models are pre-bundled in the `.paddlex` folder.

**Q: I have Python 3.13, what should I do?**
The program opens but OCR won't work. Install Python 3.12 (exactly 3.12, not newer).

**Q: My page has multiple names, which one is read?**
If you add a yellow highlight, that one is read. Otherwise the first "first name + last name" on the page.

**Q: Where are the output files saved?**
In the folder you chose under "Output Folder" (default: `PDF_Toolkit_Output`).

**Q: Is both Persian and English supported?**
Yes — the UI is English and the OCR reads both Persian and English text.

---

## 🤝 Contributing

Comments, bug reports and suggestions are welcome! Open an Issue or a Pull Request.

## 📄 License

[MIT](LICENSE) — free for personal and commercial use.

---

<div align="center">

**Made with ❤️ — zero runtime dependencies**

</div>
