# Quick Start Guide

## Prerequisites

Before you begin, ensure you have:
- Python 3.6 or higher installed
- pip (Python package manager)
- Internet connection (for translation API)

## Installation Steps

### 1. Clone the Repository

```bash
git clone https://github.com/sorenbj/BC-Translate.git
cd BC-Translate
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

This will install:
- `python-docx` - For reading and writing Word documents
- `deep-translator` - For translation using Google Translate API

### 3. Verify Installation

Test that the application works:

```bash
python translate_docx.py --help
```

You should see the help message with usage instructions.

## Basic Usage

### Translate a Document

```bash
# Auto-generate output filename (input_translated.docx)
python translate_docx.py input.docx

# Specify output filename
python translate_docx.py input.docx output.docx

# Translate from English to Danish (default)
python translate_docx.py mydoc.docx mydoc_danish.docx
```

### Advanced Options

```bash
# Specify different languages
python translate_docx.py input.docx output.docx --source en --target da

# Use short flags
python translate_docx.py input.docx output.docx -s en -t da
```

## Supported Language Codes

Common language codes you can use:
- `en` - English
- `da` - Danish
- `de` - German
- `fr` - French
- `es` - Spanish
- `it` - Italian
- `nl` - Dutch
- `sv` - Swedish
- `no` - Norwegian
- `fi` - Finnish

For a complete list, see [ISO 639-1 language codes](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes).

## Example Workflow

1. **Prepare your document**: Create or open an English Word document (`.docx`)
2. **Run the translation**:
   ```bash
   python translate_docx.py report_en.docx report_da.docx
   ```
3. **Review the output**: Open `report_da.docx` to see the translated document
4. **Check formatting**: Verify that all formatting has been preserved

## Tips

- **Large documents**: Translation may take several minutes for large documents
- **Internet required**: The application needs internet access to use Google Translate
- **Formatting**: Bold, italic, fonts, tables, and structure are all preserved
- **Images**: Images are kept as-is (not translated)
- **Rate limits**: If you get errors, wait a moment and try again (free API has limits)

## Troubleshooting

### "Module not found" error
```bash
pip install python-docx deep-translator
```

### Translation fails
- Check your internet connection
- Wait a moment if you've translated many documents (rate limiting)
- Try again - sometimes it's a temporary network issue

### File not found
- Make sure you provide the correct path to your input file
- Use absolute paths if relative paths don't work

## Getting Help

Run the help command to see all available options:
```bash
python translate_docx.py --help
```

## What's Next?

- See [EXAMPLES.md](EXAMPLES.md) for more detailed examples
- Check [README.md](README.md) for complete documentation
