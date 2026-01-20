# BC-Translate

A Python application for translating Word documents from English to Danish while preserving formatting.

## Features

- Translates Word (.docx) documents from English to Danish
- Preserves document formatting (bold, italic, fonts, etc.)
- Handles paragraphs and tables
- Simple command-line interface
- Uses Google Translate API via deep-translator

## Installation

### Prerequisites

- Python 3.6 or higher
- pip (Python package manager)

### Setup

1. Clone the repository:
```bash
git clone https://github.com/sorenbj/BC-Translate.git
cd BC-Translate
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

Or install manually:
```bash
pip install python-docx deep-translator
```

## Usage

### Basic Usage

Translate a document (output filename will be auto-generated):
```bash
python translate_docx.py input.docx
```

Specify output filename:
```bash
python translate_docx.py input.docx output.docx
```

### Advanced Options

Specify source and target languages:
```bash
python translate_docx.py input.docx output.docx --source en --target da
```

### Command-line Arguments

- `input`: Input .docx file path (required)
- `output`: Output .docx file path (optional, defaults to `input_translated.docx`)
- `--source, -s`: Source language code (default: `en` for English)
- `--target, -t`: Target language code (default: `da` for Danish)

### Examples

```bash
# Translate with auto-generated output name
python translate_docx.py document.docx

# Translate with specific output name
python translate_docx.py english_doc.docx danish_doc.docx

# Translate from English to Danish (explicit)
python translate_docx.py input.docx output.docx --source en --target da
```

## How It Works

1. **Document Loading**: The application uses `python-docx` to load the Word document
2. **Text Extraction**: Text is extracted from paragraphs and tables while preserving structure
3. **Translation**: Text is translated using Google Translate (via `deep-translator`)
4. **Formatting Preservation**: The translated text replaces the original while maintaining formatting
5. **Document Saving**: The translated document is saved with all formatting intact

## Supported Languages

The application supports any language pair supported by Google Translate. Common codes:
- `en`: English
- `da`: Danish
- `de`: German
- `fr`: French
- `es`: Spanish
- `it`: Italian
- `nl`: Dutch
- `sv`: Swedish
- `no`: Norwegian

## Limitations

- Complex formatting with multiple runs per paragraph may be simplified
- Very long documents may take time to translate due to API rate limits
- Requires internet connection for translation
- Images and embedded objects are preserved but their alt text is not translated

## Troubleshooting

### "Module not found" errors
Make sure you've installed the requirements:
```bash
pip install -r requirements.txt
```

### Translation fails
- Check your internet connection
- The free Google Translate API may have rate limits
- Very long text blocks are automatically split into chunks

## License

This project is open source and available for use.

## Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.
