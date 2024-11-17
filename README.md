# Image to Text Converter

This Python script extracts text from an image using Optical Character Recognition (OCR) via the Tesseract library. The script uses the `pytesseract` package and `Pillow` for image processing to convert the content of an image into readable text.

## Features

- **OCR with Tesseract**: Extracts text from images.
- **Cross-Platform Support**: Configured to run on Windows systems by default, but can be adapted for other platforms.
- **Simple Command-Line Interface**: The script accepts an image file path as a command-line argument, processes it, and outputs the extracted text.

## Installation

### Requirements

Ensure you have the following Python libraries installed:

- `pytesseract` (`pip install pytesseract`)
- `Pillow` (`pip install Pillow`)

You also need to install [Tesseract OCR](https://github.com/tesseract-ocr/tesseract) on your system.

- On Windows, install Tesseract and make sure the installation directory (typically `C:\Program Files\Tesseract-OCR\`) is in your system's PATH, or you can specify the path directly in the script as shown.

### Setting Up Tesseract (Windows)

1. Download the Tesseract installer from the official repository: [Tesseract GitHub](https://github.com/tesseract-ocr/tesseract).
2. Run the installer and note the installation path (e.g., `C:\Program Files\Tesseract-OCR\tesseract.exe`).
3. Update the script by ensuring the path to `tesseract.exe` is correct. This is done in the script where the `pytesseract.pytesseract.tesseract_cmd` is set.


The script will output the extracted text to the console.

## Script Breakdown

1. **`image_to_text` Function**: This function loads an image using `Pillow` and applies `pytesseract.image_to_string()` to extract text from the image.
2. **Error Handling**: If an error occurs during image processing or OCR, the script returns an error message.
3. **Command-Line Arguments**: The script expects the image path to be provided as a command-line argument. If this is missing, the script prints the usage instructions.

## Error Handling

- If no image path is provided, the script will print usage instructions.
- If an error occurs during the OCR process (e.g., incorrect image format or invalid Tesseract installation), the script will output an error message.

## License

This project is licensed under the MIT License. Feel free to use, modify, and distribute.

## Acknowledgments

- **Tesseract OCR**: For the powerful text extraction capabilities.
- **Pillow**: For handling image loading and processing.


