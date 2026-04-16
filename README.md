# Music Key Detection — DSP Pipeline
A signal processing pipeline for estimating the musical key of a track from a Spotify track ID. The pipeline downloads audio, performs harmonic-percussive source separation (HPSS), extracts chroma features using a Constant-Q Transform, and correlates against Krumhansl-Kessler key profiles to estimate the most likely major or minor key.
Pipeline:

Audio retrieval via Spotify API and yt-dlp
Harmonic-percussive separation using median filtering on the STFT
Chroma CQT feature extraction with tuning correction
Beat-synchronous chroma aggregation
Correlation against major and minor key templates (Krumhansl & Kessler, 1982)
Predominant pitch histogram via pYIN pitch estimation

## Setup:
### 1. Create Virtual Environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 2. Install Dependencies
```bash

pip install spotipy yt-dlp librosa numpy python-dotenv ffmpeg-python matplotlib
```

### 3. Install FFmpeg

- macOS: `brew install ffmpeg`

- Linux: `sudo apt install ffmpeg`

- Windows: Download from ffmpeg.org and add to PATH

### 4. Spotify Developer Setup

- Go to Spotify Developer Dashboard

- Create a new app

- Copy Client ID and Client Secret

### 5. Environment File

Create .env file:
```yml
#.env
SPOTIFY_CLIENT_ID="your_client_id_here"
SPOTIFY_CLIENT_SECRET="your_client_secret_here"
```
