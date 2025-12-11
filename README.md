Below is a clean, modern **README.md** for your Python PDF text-extraction script.

If you want it **updated for Python 3**, **turned into a module/package**, or want a **bilingual (EN/AR) README**, just tell me!

---

# 📄➡️📝 PDF Text Extraction Script (Python)

This script extracts **text content from PDF files** using **pdfminer**.
It provides a `convert()` function that takes a PDF and returns all extracted text (optionally from specific pages).

---

## 🚀 Features

* Extracts plain text from PDF files
* Optionally extract text from specific page numbers
* Uses **pdfminer** low-level API for precise parsing
* Simple `convert()` function you can reuse anywhere

---

## 📦 Requirements

This script uses the following Python libraries:

```
pdfminer
pdfquery
cStringIO (Python 2)
```

### Install:

```bash
pip install pdfminer pdfquery
```

⚠️ **Note:**
`cStringIO` and `file()` indicate this is **Python 2 code**.
If you want a **Python 3 version**, I can convert it for you.

---

## 📂 Example Usage

```python
from pdf_to_text import convert

text = convert("sample.pdf")
print(text)
```

### Extract specific pages:

```python
text = convert("sample.pdf", pages=[0, 1, 2])
print(text)
```

---

## 🧠 How It Works

### `convert(fname, pages=None)`

1. Sets the page numbers
2. Creates a `StringIO` buffer
3. Initializes:

   * PDFResourceManager
   * TextConverter
   * PDFPageInterpreter
4. Loops through PDF pages
5. Processes each page and extracts text
6. Returns the extracted text as a string

---

## ⚠️ Limitations

* This version is for **Python 2**
* `cStringIO` and `file()` are deprecated in Python 3
* `pdfminer.six` is the recommended library for Python 3

