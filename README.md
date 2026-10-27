# Gemini AudioTranscriber AI

An AI-powered audio transcription web application built with React, TypeScript, and the Google Gemini API. The application processes uploaded audio recordings in sequential 7-second segments and converts spoken content into text.

## Features

- **Audio Upload:** Upload supported audio files, including MP3, WAV, and AAC, subject to browser decoding support.
- **Automatic Audio Segmentation:** Divide recordings into 7-second segments for sequential processing.
- **AI-Powered Transcription:** Use the Gemini API to transcribe each audio segment independently.
- **Real-Time Progress Tracking:** Display processed segments, total segments, and completion percentage.
- **Segment-Level Results:** Track transcription status for individual segments, including pending, processing, completed, and failed states.
- **Error Handling:** Handle segment-level failures while allowing the remaining segments to continue processing.
- **Responsive Interface:** Provide a clean interface for uploading audio, monitoring progress, and viewing transcription results.

## Technology Stack

- React
- TypeScript
- Tailwind CSS
- Google Gemini API
- Web Audio API
- HTML and CSS

## How It Works

1. The user uploads an audio recording.
2. The application decodes the file using the browser's Web Audio API.
3. The audio is divided into segments of approximately seven seconds.
4. Each segment is converted into WAV audio and encoded as Base64.
5. The Gemini API processes each segment and returns its transcription.
6. The interface updates each segment's status and displays overall progress.

## Project Structure

```text
gemini-audio-transcriber/
├── components/
│   ├── Layout.tsx
│   └── TranscriptionView.tsx
├── services/
│   ├── audioService.ts
│   └── geminiService.ts
├── App.tsx
├── types.ts
├── package.json
└── README.md
```

*The structure above is illustrative; adjust it to match the actual repository.*

## Getting Started

1. Clone the repository.
2. Install the project's dependencies using the package manager and lockfile provided.
3. Configure the Gemini API integration securely.
4. Start the development server using the script defined in `package.json`.
5. Open the local development URL in your browser and upload an audio file.

## Security

Keep API credentials out of client-side source code and public repositories. For a deployed application, route Gemini API requests through a backend that stores the API key in an environment variable.

## Limitations

- Transcription quality depends on audio clarity, language, background noise, and the selected Gemini model.
- Sequential processing may increase the total processing time for long recordings.
- Transcribing segments independently may affect continuity, punctuation, and speaker references across segment boundaries.
- Browser audio decoding depends on the file format and browser capabilities.

## Future Improvements

- Support for multiple languages and automatic language detection.
- Speaker identification and diarization.
- Editable transcripts and TXT, SRT, or VTT export.
- Timestamped transcription and audio playback synchronization.
- Retry controls for failed segments.
- Cancellation and resumable processing.
- Secure backend integration and deployment.


