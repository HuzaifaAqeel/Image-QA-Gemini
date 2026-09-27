# Image-QA-Gemini 🖼️🤖

A Streamlit web app that lets you upload an image and ask Gemini questions about it — or leave the prompt empty for an automatic visual description. Powered by **Gemini 2.5 Flash** via the `google-genai` SDK.

## What it does

- 📤 Upload a JPG, JPEG, or PNG image through a simple web UI
- ❓ Ask any question about the image ("What objects are in this photo?", "Extract the text from this receipt")
- ✨ Leave the input blank and Gemini automatically describes the image
- ⚡ Get instant answers from Google's Gemini 2.5 Flash vision model

## Tech stack

- [Streamlit](https://streamlit.io/) — web UI
- [Google Gemini API (`google-genai`)](https://ai.google.dev/) — vision + language model (`gemini-2.5-flash`)
- [Pillow (PIL)](https://pillow.readthedocs.io/) — image handling
- [python-dotenv](https://github.com/theskumar/python-dotenv) — environment variable management

## Run it yourself

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Set your Gemini API key (get a free one at [Google AI Studio](https://aistudio.google.com/app/apikey)):
   ```bash
   export GOOGLE_API_KEY="your_api_key_here"
   ```
   (or create a `.env` file in the project root with `GOOGLE_API_KEY=your_api_key_here`)

3. Launch the app:
   ```bash
   streamlit run vision.py
   ```

4. Open the browser link Streamlit prints, upload an image, type a question, and hit **Ask the Question**.

## Project structure

```
.
├── vision.py         # Main Streamlit app + get_gemini_response()
├── requirements.txt  # Python dependencies
├── .gitignore        # Keeps .env and other secrets out of git
└── README.md         # This file
```

## Credits & license

This project is based on the original open-source project [**Gemini-Vision-App**](https://github.com/Mayur-Wasnik/Gemini-Vision-App) by [Mayur Wasnik](https://github.com/Mayur-Wasnik) (MIT License — see the [LICENSE](LICENSE) file).

Extended and maintained by **Muhammad Huzaifa Aqeel** ([HuzaifaAqeel](https://github.com/HuzaifaAqeel)):
- Migrated fully to the `google-genai` SDK with `gemini-2.5-flash`
- Added the missing `pillow` dependency to `requirements.txt`

> ⚠️ **Security note:** never commit your `.env` file or API key — it is already listed in `.gitignore`.
