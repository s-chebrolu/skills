---
name: pdf-extraction
description: Extracts text from PDF files and returns clean content. Use this skill when a user gives a PDF or asks to get text from one.
---

## Extract PDF text

This skill is for pulling text out of PDF files and cleaning it up so it’s actually readable.

Use pdfplumber for text extraction:

```python
import pdfplumber

with pdfplumber.open("file.pdf") as pdf:
    text = pdf.pages[0].extract_text()
```


## How it works

1. **Load the PDF**
   - Get the file from the given path or input

2. **Extract text**
   - Use a reliable library (default to `pdfplumber`)
   - Go through each page and collect the text

3. **Clean the text**
   - Remove extra spaces and weird line breaks
   - Keep paragraphs readable when possible

4. **Handle edge cases**
   - If no text is found, the PDF might be scanned
   - In that case, mention that OCR might be needed


## Output format

Return: extracted and cleaned text


## Guidelines

- Keep the output clean and easy to read
- Don’t list a bunch of tools
- Stick to one solid method unless there’s a reason not to
- Focus on giving useful text, not explaining every detail


## File access

If needed, use:
- `scripts/extract_text.py`

#IMPORTANT: Only use the script if basic extraction doesn’t work well. Do NOT use this skill for editing or creating PDFs and/pr working with images unless text extraction is needed.
