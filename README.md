# AI Text Summarizer

An AI-powered web application that converts long text into concise, meaningful summaries using the T5 Transformer model from Hugging Face. Built with Python and FastAPI, the application provides a simple web interface for generating summaries efficiently.

## Features

- AI-Powered Summarization: Uses the Hugging Face T5 Transformer to generate concise summaries.
- FastAPI Backend: Provides API endpoints for processing text and returning summaries.
- Web Interface: Allows users to interact with the summarization application through a browser.
- Optimized Text Processing: Uses tokenization and attention masks to prepare input text for the model.
- Pretrained Model Support: Supports loading a locally saved summarization model.
- Configurable Generation: Controls summary length and beam search parameters to generate summaries.

## Tech Stack

- Programming Language: Python
- AI/ML Model: T5 Transformer
- Model Library: Hugging Face Transformers
- Deep Learning Framework: PyTorch
- Backend Framework: FastAPI
- Server: Uvicorn
- Frontend: HTML, CSS, JavaScript
- Model Hub: Hugging Face

## Project Structure

TEXTSUMMARISER/
├── app.py
├── index.html
├── saved_summary_model/
├── requirements.txt
├── README.md
└── .gitignore

Note: The "saved_summary_model/" directory contains the locally saved model, if applicable. Large model files may need to be downloaded separately.

## How It Works

1. The user enters long text through the web interface.
2. The application receives the text through a FastAPI endpoint.
3. The tokenizer converts the input text into token IDs and an attention mask.
4. The T5 Transformer generates a concise summary using text generation.
5. The generated token IDs are decoded into readable text.
6. The application returns the summary to the user.

## Installation and Setup

1. Clone the repository

### git clone https://github.com/batham04/TextSummariser.git
cd TextSummariser

2. Create a virtual environment

python -m venv .venv

Activate it on Windows:

### .venv\Scripts\activate

3. Install dependencies

If a "requirements.txt" file is available:

### pip install -r requirements.txt

Otherwise, install the main dependencies:

### pip install fastapi uvicorn transformers torch sentencepiece jinja2

4. Configure the model

Ensure the required T5 model and tokenizer are available. If the application loads a locally saved model, configure the model path in "app.py" to match your local directory.

5. Run the application

### uvicorn app:app --reload

6. Open the application

Visit the following URL in your browser:

### http://127.0.0.1:8000

You can also access the FastAPI interactive API documentation at:

### http://127.0.0.1:8000/docs

API Endpoint

### "POST /summarize/"

Accepts text input and returns an AI-generated summary.

The exact request schema depends on the application's "DialogueInput" model.

Example response:

{
  "summary": "This is an example of a concise generated summary."
}

The response above is illustrative; actual output depends on the submitted text and model.

## Model Details

The application uses a T5 (Text-to-Text Transfer Transformer) model for abstractive text summarization. T5 treats text tasks as text-to-text problems and generates a summary based on the supplied input.

Generation parameters can be adjusted to control the length and quality of the output.

## Future Improvements

- Support longer input documents.
- Add file upload support for text and PDF documents.
- Improve the user interface and user experience.
- Add summary length controls.
- Deploy the application to a cloud platform.

## Contributing

Contributions, suggestions, and improvements are welcome. Feel free to fork the repository and submit a pull request.

## License

This project is licensed under the MIT License, provided the repository includes the corresponding "LICENSE" file.

---

Built with Python, FastAPI, and Hugging Face Transformers.
