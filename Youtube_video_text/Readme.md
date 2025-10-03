# Video Transcription Workflow Using Google Gemini API & n8n

![Workflow Animation](https://media.giphy.com/media/l0MYt5jPR6QX5pnqM/giphy.gif)

## Overview

This workflow automates transcribing spoken dialogue from YouTube videos using **Google’s Generative AI Gemini API** combined with the low-code power of **n8n**. It efficiently processes multimodal inputs (video/audio) and generates verbatim text transcripts within minutes.

---

## Features

- Uses the advanced **`gemini-2.5-flash`** model for multimodal transcription.
- Fast transcription: ~1 min 8 sec for a 13-minute video.
- Easy integration and customization inside the visual n8n workflow builder.
- Open source and ready to deploy in your own environment.

---

## Getting Started

### Prerequisites

- Google Cloud account with Generative AI (Gemini) API enabled.
- API Key generated from Google Cloud Console.
- n8n instance or access to n8n.cloud.
- Basic familiarity with HTTP webhooks and JSON.

### Installation

1. Download or clone this repository.
2. Import the `workflow.json` file into your n8n instance.
3. Update the environment variables:
   - Replace `YOUTUBE_API_KEY` with your actual Google API key.
4. Activate the workflow and expose webhook URLs.
5. Use a POST request with YouTube URL and API key to start transcription.

---

## Usage

Send the following JSON payload to the webhook URL:

{
"youtubeURL": "https://youtu.be/<video_id>",
"apiKey": "<Your_Google_API_Key>",
"promptType": "transcript",
"automationID": "optional-reference"
}


The workflow returns the transcribed video dialogue text in JSON format.

---

## Contributing

Feel free to fork and extend this workflow! Pull requests and issues are welcome.

---

## License

This project is licensed under the MIT License.
