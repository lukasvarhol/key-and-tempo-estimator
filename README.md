### 1. Create Virtual Environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 2. Install Dependencies
```bash

pip install spotipy yt-dlp librosa numpy python-dotenv ffmpeg-python
```

### 3. Install FFmpeg

    macOS: ```brew install ffmpeg```

    Linux: ```sudo apt install ffmpeg```

    Windows: Download from ffmpeg.org and add to PATH

### 4. Spotify Developer Setup

    Go to Spotify Developer Dashboard

    Create a new app

    Copy Client ID and Client Secret

### 5. Environment File

Create .env file:
```yml
#env

SPOTIFY_CLIENT_ID=your_client_id_here
SPOTIFY_CLIENT_SECRET=your_client_secret_here
```
