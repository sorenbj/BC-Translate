# BC-Translate Examples

This directory contains example documents for testing the translation functionality.

## Creating Test Documents

You can create your own test documents using Microsoft Word or LibreOffice Writer, or use the Python script below:

```python
from docx import Document

# Create a new Document
doc = Document()
doc.add_heading('My Document', 0)
doc.add_paragraph('This is a test paragraph.')
doc.save('example.docx')
```

## Testing the Application

1. Create or use an existing Word document in English
2. Run the translation:
   ```bash
   python translate_docx.py your_document.docx
   ```
3. The translated document will be saved as `your_document_translated.docx`

## What Gets Translated

- ✅ Headings and titles
- ✅ Paragraphs
- ✅ Table contents
- ✅ List items
- ✅ Text with formatting (bold, italic, etc.)

## What Gets Preserved

- ✅ Document structure
- ✅ Text formatting (bold, italic, underline, etc.)
- ✅ Font styles and sizes
- ✅ Tables and their structure
- ✅ Lists (bulleted and numbered)
- ✅ Headers and footers
- ✅ Images and embedded objects (not translated, but preserved)
