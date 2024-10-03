# Optical Character Recognition (OCR) Application

This Optical Character Recognition (OCR) app allows users to extract text from images using Python's `pytesseract` library and the Tesseract-OCR engine. The app features a simple web interface where users can upload images and see the extracted text.

## Features

- **Image Upload**: Upload an image to extract text using OCR.
- **Text Extraction**: View the extracted text on the same page.
- **User-Friendly Interface**: Simple and intuitive UI built using Materialize CSS.
- **Sample Data**: Sample images are available in the `sample_data` folder for testing.

## Prerequisites

- Python or [Anaconda](https://www.anaconda.com/) installed.
- [Tesseract-OCR](https://github.com/UB-Mannheim/tesseract/wiki) installed (for Windows users).
- Basic understanding of Python and the command line.

## Installation and Setup

To set up and run the application on your local machine, follow these steps:

### Step 1: Clone the repository
Clone this repository to your local machine using the following command:
```bash
git clone <repository-url>
```


### Step 2: Navigate to the project directory
Open a command prompt or terminal, and change your current directory to where the app.py file is located:

```bash
cd <project-folder-path>
```

### Step 3: Create a Python environment
Create a new environment for the project using Anaconda:

```bash
conda create --name <environment-name> python=3.8
```
Alternatively, you can use venv or a different environment manager if you don't use Anaconda:

``` bash
python -m venv <environment-name>
```

### Step 4: Activate the environment
Activate the created environment:

```bash
conda activate <environment-name>
```
Or for venv users:

```bash
source <environment-name>/bin/activate  # On Linux/Mac
<environment-name>\Scripts\activate     # On Windows
```

### Step 5: Install Tesseract

### Step 6: Set the Tesseract Path
After installation, note the path of tesseract.exe (default: C:\Program Files\Tesseract-OCR\tesseract.exe). In the Python code, specify the path as follows:


```python
pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'
```
### Step 7: Install required dependencies
Install the dependencies listed in the requirements.txt file:

```bash
python -m pip install -r requirements.txt
```
This will install libraries such as Flask, pytesseract, and others required to run the application.

### Step 8: Run the application
Start the Flask application by running:

```bash
python app.py
```
The app will start running on your local server, and you will see an output like:

```csharp
 * Running on http://127.0.0.1:5000/
 ```

### Step 9: Open the application in your browser
Open the provided URL (http://127.0.0.1:5000/) in your web browser to view the app.

### Step 10: Test the app with sample data
In the sample_data folder, you can find sample images for testing. Upload one of these images to see the extracted text.

## Troubleshooting
### Common Errors and Fixes
Tesseract Not Found: If you encounter an error like TesseractNotFoundError, make sure that:

- Tesseract is installed properly.
- The path to tesseract.exe is correctly set in the Python script.

Missing Dependencies: If any library is missing, try running:

```bash
python -m pip install <library-name>
```
This could happen if a dependency is not properly installed via requirements.txt.

Virtual Environment Not Activating: Ensure that you're using the correct environment. For Conda users, ensure you've activated the environment using:

```bash
conda activate <environment-name>
```
Permission Issues on Windows: If you're running into permission issues on Windows, try running your command prompt or terminal as an administrator.