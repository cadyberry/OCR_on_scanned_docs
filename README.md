# OCR on Scanned Documents

A Python pipeline for extracting and analyzing text from scanned document images. Upload an image, get back structured information — no manual transcription needed.

## What it does

1. **OCR** — extracts raw text from a scanned image using Tesseract
2. **Summarization** — condenses the extracted text using Facebook BART (`facebook/bart-large-cnn`)
3. **Named entity recognition** — identifies people, organizations, and locations using a fine-tuned BERT model
4. **Chained pipeline** — one function call runs all three steps and saves results to file

Built and run in Google Colab. Useful for processing contracts, forms, archived documents, or any text that exists only as an image.

## Stack

- `pytesseract` + Tesseract OCR — text extraction
- `transformers` (Hugging Face) — summarization and NER
- `Pillow` — image handling
- Google Colab — runtime environment

## Quick start

Open the notebook in [Google Colab](https://colab.research.google.com/), then run cells top to bottom. When prompted, upload a scanned image (JPG or PNG).

```
OCR_and_NLP_with_Scanned_Documents.ipynb
```

The notebook installs all dependencies automatically.

## Output

- `extracted_text.txt` — raw OCR output
- `summary.txt` — BART-generated summary
- Named entities printed inline with confidence scores