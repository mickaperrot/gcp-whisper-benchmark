GCP vs Whisper Benchmark
This repository provide tools to benchmark Speech-to-Text (STT) solutions from Google Cloud (Chirp) & OpenAI (Whisper).

It is structured into 3 folders:
1) Audio_conversion: tool to convert .mp4 video to audio files compatible with Chirp & Whisper
2) Transcript_generation: tool to generate TXT and SRT transcripts
3) WER_calculation: tools to calculate WER scores and analyze transcript quality

Prerequisites
You must have a Google Cloud project with billing enabled.

All the notebooks in this repository have been tested on Vertex AI Workbench notebook.
The Notebooks API must be enabled.

Create a Vertex AI Workbench notebook:
- Operating suystem: Debian 11
- Environment: Python 3 (with Intel MKL)

Open the notebook.
Clone this repository.

Convert video files
Create a Google Cloud Storage bucket.
Grant the "Storage Admin" role on the bucket to the default GCE service account.
Create a folder in the bucket to store video files.
Import videos into subfolders named after the language code of the source audio.
For example:

Run the notebook Audio_conversion/convert_video_to_audio.ipynb
Set in the 1st cell the GCS URI to the video files from the previous step and the target GCS URI to store the audio files.
Run all the cells.
When complete, audio files should be available in the target GCS folder.
