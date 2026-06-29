# AI Video Assistant

This repository contains a Streamlit-based AI meeting assistant for transcribing audio or video content, summarizing meetings, extracting action items, and answering questions using a RAG chat interface.

## Structure
- `app.py`: Streamlit UI and pipeline orchestration
- `main.py`: CLI entry point for running the pipeline from the command line
- `core/`: meeting analysis logic including transcription, summarization, extraction, and the RAG chain
- `utils/audio_processor.py`: audio download, conversion, and chunking helpers
- `requirements.txt`: Python dependency list

## Setup
1. Install Python 3.10+.
2. Create and activate a virtual environment:
   ```bash
   python -m venv .venv
   .venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Add a `.env` file with the required API keys and model settings, for example:
   ```text
   MISTRAL_API_KEY=your_mistral_api_key
   WHISPER_MODEL=small
   SARVAM_API_KEY=your_sarvam_api_key
   SARVAM_STT_MODEL=saaras:v2.5
   ```
5. Run the Streamlit app:
   ```bash
   streamlit run app.py
   ```

## Notes
- `ffmpeg` must be installed separately for audio conversion.
- Do not commit `.env`, `.venv`, or downloaded media files.
