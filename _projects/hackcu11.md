---
layout: page
title: Take-a-Note – AI-Powered Note-Taking App
description: HackCU11 project using Whisper & GPT-4 for real-time transcription and summarization
img: /assets/img/takeanote/take_home.png
importance: 2
category: School
---

## Project Overview

Take-a-Note is a real-time, AI-powered note-taking application developed during HackCU11.  
The application transcribes and summarizes audio and video content by combining OpenAI’s Whisper model for speech-to-text and GPT-4 for intelligent summarization.

Designed to assist students and professionals during lectures and meetings, the app automates the creation of structured, concise notes from raw spoken content, helping users save time and stay focused.
<br><br>

---

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/takeanote/take_home.png" title="App UI – Summarized Notes" class="img-fluid rounded z-depth-1" %}
  </div>
</div>

<div class="caption">
  The app processes audio and video files up to 25MB and returns clean, accurate summaries in under 10 seconds.
</div>

---

## Project Features

- Transcribes speech from uploaded audio and video files using OpenAI Whisper.
- Generates concise and structured summaries using GPT-4.
- Designed for speed and usability—end-to-end processing takes less than 10 seconds.
- Simple and clean web interface for file upload and results display.
- Supports .mp3 and .mp4 formats.
<br><br>

<div class="row">
  <div class="col-sm mt-2 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/takeanote/take_quiz.png" title="App UI – Summarized Notes" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm mt-2 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/takeanote/take_trans.png" title="App UI – Summarized Notes" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<br><br>

---
## My Focus 

I was responsible for **all back-end development** of the application.  
This included designing and implementing the server-side logic for:

- Handling file uploads and preprocessing.
- Integrating the **OpenAI Whisper API** for real-time transcription.
- Calling the **GPT-4 API** to generate context-aware summaries.
- Optimizing the API pipeline for performance and reliability.
- Ensuring clean input-output flow between front-end and AI services.

My focus was on making the system fast, stable, and easily extendable, with modular endpoints for different file types and formats.
<br><br>

---

## Technical Stack

- **Frontend:** HTML, CSS, Bootstrap  
- **Backend:** Python, Flask  
- **AI/ML:** OpenAI Whisper (ASR), GPT-4 (NLP summarization)  
- **Audio Processing:** Pydub, FFmpeg  
- **Deployment:** Replit, GitHub, Devpost
<br><br>

---

## Live Demo and Code

- [Devpost Project Page](https://devpost.com/software/take-a-note?ref_content=my-projects-tab&ref_feature=my_projects)  
- [GitHub Repository](https://github.com/Ales4999/takeanote) 
<br><br>

---

## Hackathon Reflection

Take-a-Note was built in under 24 hours during HackCU11 as a proof-of-concept for real-time, AI-driven productivity tools.  
The project demonstrated how integrating speech recognition with large language models can result in a powerful, accessible tool for summarizing dense content with minimal user effort.

