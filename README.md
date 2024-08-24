
# Text to Document API

This is a Flask API that accepts unstructured text, processes it using NLP (spaCy) to extract named entities, and then generates a Word document with the structured information.

## Requirements

- Python 3.x
- pip

## Installation

1. Clone this repository or download the files.
2. Navigate to the project directory.
3. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Download the necessary spaCy model:

   ```bash
   python -m spacy download en_core_web_sm
   ```

## Running the Application

To run the application:

```bash
python app.py
```

The API will be available at `http://127.0.0.1:5000`.

## Usage

You can make a POST request to the `/generate-doc` endpoint with a JSON payload containing the `text` field. For example:

```bash
curl -X POST http://127.0.0.1:5000/generate-doc -H "Content-Type: application/json" -d "{"text": "Barack Obama was born in Honolulu, Hawaii, on August 4, 1961."}"
```

This will generate a Word document with the original text and the extracted entities.

## Notes

- The generated document will be saved as `generated_document.docx` in the root directory of the project.
- You can use tools like `curl` or `Postman` to test the API.
