# Tabby
# AI Guitar Tab Transcription Tool

An AI-powered web tool that transcribes songs into guitar tabs for 6-string guitars. The tool isolates the guitar part from an audio track, generates a guitar tab, and provides features like fretboard visualization and synchronized track playback.
---
This project is intended for educational purposes only. The use of this code for commercial purposes or to gain personal or financial profit is strictly prohibited. Any attempts to use this code for personal gain or in a commercial product will be subject to legal consequences.
---

## Features:
- **AI Transcription:** Uses the **Demucs** model to isolate the guitar track from other instruments.
- **Guitar Tab Generation:** Converts the isolated guitar audio into **guitar tabs** using the **Basic Pitch** model.
- **Visualizations:**
  - Guitar **tab** view.
  - **Fretboard** visualization for better learning.
  - **Synchronized playback** of the transcribed guitar part alongside the original track.
- **User Accounts:** Users can sign up, log in, and save their transcriptions.
- **History:** Users can view their past transcriptions.

---

## Technology Stack:
### Frontend:
- **React** – For building the interactive user interface.
- **Tailwind CSS** – For responsive and customizable styling.
- **Firebase Authentication** – For user login and registration.
- **Firebase Storage** – For storing uploaded audio files.

### Backend:
- **FastAPI** – For handling API requests and processing audio files.
- **Demucs** (Python) – For separating the guitar part from the audio.
- **Basic Pitch** (Python) – For converting the isolated guitar audio to MIDI and generating guitar tabs.

### Deployment:
- **Railway** – For backend API hosting.
- **Vercel** or **Firebase Hosting** – For frontend hosting.

---

## How It Works:

### 1. **User Uploads Audio**
   - The user uploads an audio file (MP3, WAV, etc.) via the frontend.
   - The audio file is uploaded to **Firebase Storage**.

### 2. **Backend Processes the Audio**
   - The **FastAPI backend** receives the uploaded file from Firebase Storage.
   - The backend uses **Demucs** to isolate the guitar part from the rest of the track (drums, vocals, etc.).
   - The isolated guitar audio is then passed to **Basic Pitch** for conversion into **MIDI data** and **guitar tab** format.

### 3. **Visualize the Guitar Tab**
   - The generated guitar tab is sent to the frontend and displayed for the user.
   - A **fretboard** visualization is also shown to help users visualize the finger placements.
   - A **synchronized track** allows users to follow along with the transcribed guitar part.

### 4. **Save and View Transcriptions**
   - Registered users can save their transcriptions and view past submissions.

---

## Setup & Development

### Prerequisites:
1. **Install Node.js** (for frontend) and **Python 3.x** (for backend).
2. Set up **Firebase** for user authentication and storage.

### Clone the Repository:
```bash
git clone https://github.com/<your-username>/ai-guitar-tab-transcription.git
