🎙️ Goremi's Audio Translator (Speech to Text Converter)

A clean and simple desktop application built with Python and the Flet framework to convert audio files (.wav format) into text transcripts using the Google Speech Recognition API.

✨ Features

Simple UI: A clean, single-window interface designed with Flet.

WAV File Transcription: Supports uploading and transcribing local .wav audio files.

Google Recognition: Utilizes the speech_recognition library to connect to the Google Speech Recognition service.

Error Handling: Provides clear messages for successful transcription, unknown audio (no speech detected), API connection issues, and file errors.

Save Functionality: Allows the user to save the resulting transcription as a plain text file (.txt).

Custom Styling: Features a bold purple background and vibrant button styling.

⚙️ Prerequisites

To run this application, you need to have Python installed on your system, along with the required libraries.

Python Environment Setup

The application relies on the following Python packages:

Flet: For the cross-platform desktop UI.

SpeechRecognition: For handling audio and interfacing with the transcription service.

PyAudio (Required Dependency): Necessary for the SpeechRecognition library to work correctly with system audio, although this app uses files.

You can install all dependencies using pip:

pip install flet SpeechRecognition
# You may also need to install the PyAudio dependency separately 
# depending on your operating system (e.g., using pip or apt/brew)


Note: On some systems, installing PyAudio might require system-level dependencies like portaudio.

🚀 How to Run the Application

Save the Code: Save the provided Python code as a file named speech_app.py.

Open Terminal: Navigate to the directory where you saved the file.

Run the Script: Execute the file using the Python interpreter:

python speech_app.py


The desktop application window will open immediately.

📝 Usage

Start: The application window opens with the title Goremi's Speech to Text Converter.

Upload: Click the "Upload Audio File" button. This will open your system's file browser.

Select File: Choose a local audio file in the .wav format.

Transcribe: The application will immediately begin processing the audio and display the resulting text in the white output box.

Save: If the transcription is successful, click the "Save Transcription" button. A save dialog will appear, allowing you to choose a location and filename for your .txt transcription file.

🛠️ Development Details

The application is encapsulated within the main(page: ft.Page) function, which is the entry point for Flet apps.

Component

Responsibility

ft.FilePicker()

Manages file selection for both uploading audio and saving the text file.

transcribe_audio(file_path)

Core logic function. Uses speech_recognition.Recognizer() and the recognize_google() method to perform the transcription.

output_text

A simple ft.Text widget used as the main console/output display for feedback.

Styling

Uses a purple (page.bgcolor = "purple") theme with custom button colors (#62FF00 for transcribe) for a distinct look.

📦 Future Improvements

Add support for more audio formats (e.g., MP3, FLAC) using libraries like pydub.

Implement a progress bar or loading spinner during transcription, as recognize_google is a blocking call.

Allow language selection for transcription (e.g., r.recognize_google(audio, language="es-ES")).

Integrate a logging mechanism for tracking API requests and errors.

Created by GoremiOguru
