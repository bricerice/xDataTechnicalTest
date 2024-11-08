# xDataTechnicalTest
HTX xData Technical Test Question – Data Scientist
# ASR Microservice

This repository contains a microservice that uses the `wav2vec2-large-960h` model for Automatic Speech Recognition (ASR) to transcribe audio files.

## Setup

1. Clone the repository:
    ```bash
    git clone https://github.com/fred/myrepo.git
    cd myrepo
    ```

2. Create a virtual environment and install dependencies:
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    pip install -r requirements.txt
    ```

3. Run the API:
    ```bash
    python asr/asr_api.py
    ```

    The service will be available at `http://localhost:8001`.

## Endpoints

### /ping (GET)
- **Description**: Checks if the service is running.
- **Response**: `pong`

### /asr (POST)
- **Description**: Transcribes an audio file.
- **Parameters**: 
  - `file`: Audio file in `mp3` format.
- **Response**:
    ```json
    {
      "transcription": "Transcribed text",
      "duration": "File duration in seconds"
    }
    ```

## Docker Setup

1. Build the Docker image:
    ```bash
    docker build -t asr-api .
    ```

2. Run the container:
    ```bash
    docker run -p 8001:8001 asr-api
    ```

## License
MIT License
