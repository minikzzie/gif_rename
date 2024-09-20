# GIF Renamer Program

## Overview
This Python program renames GIF files based on the text extracted from the GIF using the Tesseract OCR engine. The program categorizes the renamed GIFs into three folders based on the accuracy of the extracted text: 
- High Accuracy (90-100%)
- Medium Accuracy (50-90%)
- Low Accuracy (<50%) or Error

Each renamed GIF file will have a corresponding entry in a CSV file stored in the same directory. The CSVs will contain both the original filename and the new filename for reference.

## Motivation
This program was created as part of the requirement to rename a large collection of GIFs based on their content, with specific focus on GIFs needed for the **"Sign with Robert"** project. This project can be found on GitHub: [two-way-sign](https://github.com/minikzzie/two-way-sign).

## Features
- Rename GIF files based on text content extracted using Tesseract OCR.
- Sort GIFs into directories based on accuracy thresholds.
- Avoids duplicating words in filenames.
- Logs original and new filenames in CSV files.
- Skips files that are in use by another process (i.e., file locked by another application).
- Option to enable/disable debug mode for detailed logging.

## Dependencies
The following dependencies are required to run the program:
- Python 3.x
- Tesseract OCR
- Python Libraries:
  - `pytesseract`
  - `Pillow`
  - `shutil`
  - `csv`
  - `os`
  - `tkinter`

## Installation

### 1. Install Python
Make sure you have Python 3.x installed on your system. You can download it from the [official website](https://www.python.org/downloads/).

### 2. Install Tesseract OCR
Tesseract OCR must be installed and configured to work with the program. You can download it from [here](https://github.com/tesseract-ocr/tesseract).

Once installed, configure the `pytesseract.pytesseract.tesseract_cmd` to point to the Tesseract executable.

```python
pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'
