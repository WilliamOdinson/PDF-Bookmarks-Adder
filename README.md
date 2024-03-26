# PDF Bookmarks Adder

This tool is used for bookmark files in Markdown format and adds these bookmarks to a specified PDF document.

## System Requirements

Before using this tool, please make sure the following necessary Python libraries are installed on your system:

- `fitz` (also known as PyMuPDF): A high-performance library for PDF processing.

You can install any missing libraries using the pip command-line tool:

```bash
pip install PyMuPDF
```

## Usage Guide

1. Prepare your bookmark file, which needs to be extracted from the source document using OCR or other methods, and saved in Markdown (.md) format. Bookmarks should be presented in Markdown's heading format, with each bookmark's title followed by an `@` symbol and the corresponding page number. Please place this file in the `input` directory.

   Bookmark file example:

   ```markdown
   # Chapter 1 @10
   ## Section 1.1 @12
   ## Section 1.2 @14
   # Chapter 2 @20
   ```

2. Place the PDF file to which you want to add bookmarks in the `input` directory.

3. Update the following path configurations in the `main.ipynb` file:

   - `bookmarks_md_path`: The path to the bookmark Markdown file.
   - `pdf_path`: The path to the source PDF file.
   - `output_pdf_path`: The path to the output PDF file with bookmarks.

4. Execute the script to add bookmarks to the PDF file.