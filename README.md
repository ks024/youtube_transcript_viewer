#### Overview
This repository contains a Streamlit application that fetches transcripts from YouTube videos using the `youtube_transcript_api`. The application allows users to enter a YouTube video URL, fetch its transcript, and optionally download it as a text file.

#### Files Included
- **`app.py`**: Python script containing the Streamlit application code.
- **`requirements.txt`**: List of Python dependencies required for the application.
- **`Dockerfile`**: Dockerfile to build the Docker image for the Streamlit application.
- **`README.md`**: This file, providing instructions and information about the repository.

#### Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/ks024/youtube-transcript-viewer.git
   cd youtube-transcript-viewer
   ```

2. **Build the Docker Image**
   - If you want to build the Docker image locally:
     ```bash
     docker build -t youtube-transcript-app .
     ```
     Replace `youtube-transcript-app` with your desired image name.

3. **Run the Docker Container**
   - Run the Docker container using the built image:
     ```bash
     docker run -p 8501:8501 youtube-transcript-app
     ```
     This command maps port 8501 on your local machine to port 8501 inside the Docker container where Streamlit is running.

4. **Access the Application**
   - Open a web browser and go to `http://localhost:8501` to use the YouTube Transcript Viewer application.

#### Using the Docker Image from Docker Hub

If you prefer to use the Docker image that has already been uploaded to Docker Hub (`rajtmg/youtube_transcript_viewer:v1`), follow these steps:

1. **Pull the Docker Image**
   ```bash
   docker pull rajtmg/youtube_transcript_viewer:v1
   ```

2. **Run the Docker Container**
   ```bash
   docker run -p 8501:8501 rajtmg/youtube_transcript_viewer
   ```

3. **Access the Application**
   - Open a web browser and go to `http://localhost:8501` to use the YouTube Transcript Viewer application.

#### Notes
- Ensure Docker is installed and running on your machine before attempting to build and run the Docker image.
- Adjust the Docker commands (`docker build`, `docker run`, `docker pull`) as necessary based on your specific setup and preferences.
