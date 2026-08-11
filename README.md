# Google-workspace-

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Description 📝

This project appears to be a Python script designed for interacting with Google Workspace APIs, specifically focusing on live audio and video communication with AI models. It allows for real-time input and output of audio and video (from camera or screen capture) to a Google AI model, as well as text-based interaction. The script leverages Google's generative AI capabilities, `opencv-python` for video processing, `pyaudio` for audio handling, and `mss` for screen capturing.

It seems to be a personal project or experiment rather than a fully-fledged CLI tool as initially suggested by the repository name and description. The core functionality revolves around establishing a live connection with a Gemini model, enabling conversational AI with multimedia support.

## Table of Contents 📚

- [Features](#features--)
- [Tech Stack](#tech-stack--)
- [Installation](#installation--)
- [Usage](#usage--)
- [Project Structure](#project-structure--)
- [API Reference](#api-reference-conceptual--)
- [Contributing](#contributing--)
- [License](#license--)
- [Important Links](#important-links--)
- [Footer](#footer--)

## Features ⭐

- 🎤 **Live Audio Input/Output:** Captures audio from the microphone and plays back AI-generated audio in real-time.
- 🎥 **Video Input:** Supports capturing video from the default camera.
- 🖥️ **Screen Capture:** Allows for real-time screen sharing as input to the AI model.
- 💬 **Text Interaction:** Enables users to send text messages to the AI and receive text responses.
- 🤖 **AI Integration:** Connects to Google's generative AI models (specifically `gemini-2.5-flash-native-audio-preview-12-2025`).
- 🌐 **Real-time Communication:** Utilizes asynchronous programming with `asyncio` for efficient real-time data handling.
- 🎛️ **Configuration:** Provides command-line arguments to select the video input mode (`camera`, `screen`, `none`).
- 🧠 **Context Management:** Implements `ContextWindowCompressionConfig` to manage conversation context effectively.

## Tech Stack 💻

- **Language:** Python 🐍
- **Libraries:**
  - `google-genai`: For interacting with Google's generative AI models.
  - `opencv-python`: For video frame capture and processing.
  - `pyaudio`: For real-time audio stream handling.
  - `pillow` (PIL): For image manipulation.
  - `mss`: For efficient screen capturing.
  - `asyncio`: For asynchronous programming.
  - `argparse`: For command-line argument parsing.

## Installation 🛠️

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/rananisarsb51214-web/Google-workspace-.git
    cd Google-workspace-
    ```

2.  **Install Dependencies:**
    Make sure you have Python 3.7+ installed.
    ```bash
    pip install google-genai opencv-python pyaudio pillow mss
    ```

3.  **Set Environment Variable:**
    Obtain an API key from Google AI Studio and set it as an environment variable:
    ```bash
    export GEMINI_API_KEY='YOUR_GOOGLE_API_KEY'
    ```
    *(Replace `YOUR_GOOGLE_API_KEY` with your actual API key.)*

4.  **Important Note on Audio:**
    This script uses the system's default audio input/output. For optimal performance and to prevent the model from interrupting itself, it is **highly recommended to use headphones**.

## Usage ▶️

Run the Python script `Get_started_LiveAPI.py` from your terminal. You can specify the video mode using the `--mode` flag:

-   **Camera Mode (Default):**
    ```bash
    python Get_started_LiveAPI.py
    ```
    or
    ```bash
    python Get_started_LiveAPI.py --mode camera
    ```

-   **Screen Share Mode:**
    ```bash
    python Get_started_LiveAPI.py --mode screen
    ```

-   **No Video Mode:**
    ```bash
    python Get_started_LiveAPI.py --mode none
    ```

Once the script is running, you can interact with the AI by typing messages in the console and pressing Enter. Type 'q' to exit.

### Real-world Use Cases 🌍

-   **Interactive AI Assistant:** Engage in spoken or typed conversations with an AI that can understand visual context from your camera or screen.
-   **Live Tutoring/Support:** Provide real-time visual assistance where the AI can see what you're seeing (via screen share) and offer guidance.
-   **Creative Brainstorming:** Use visual input to spark ideas and generate creative content with the AI.
-   **Accessibility Tools:** Develop tools that can interpret visual information for users who might need auditory descriptions.

## Project Structure 📁

```
Google-workspace-/
├── Get_started_LiveAPI.py
├── README.md
└── LICENSE
```

## API Reference (Conceptual) 💡

The script interacts with the Google Generative AI API, specifically using:

-   `genai.Client` for API authentication and client initialization.
-   `genai.aio.live.connect` to establish a live, bidirectional connection with a specified model.
-   `types.LiveConnectConfig` for configuring the live session, including response modalities (audio) and speech configurations.
-   `types.Content` and `types.Part` for sending text and media content to the model.
-   `session.send_realtime_input` for sending audio and media data.
-   `session.receive` for processing incoming data (audio and text) from the model.

## Contributing 🤝

As this appears to be a personal project, contributions may not be actively solicited. However, if you wish to contribute:

1.  Fork the repository.
2.  Create a new branch (`git checkout -b feature/your-feature-name`).
3.  Make your changes.
4.  Commit your changes (`git commit -m 'Add some feature'`).
5.  Push to the branch (`git push origin feature/your-feature-name`).
6.  Open a Pull Request.

Please ensure your code adheres to the existing style and includes necessary documentation.

## License 📄

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Important Links 🔗

-   **Repository:** [Google-workspace-](https://github.com/rananisarsb51214/Google-workspace-)
-   **Google AI Studio:** [https://aistudio.google.com/](https://aistudio.google.com/)

## Footer 🚀

This project was developed by rananisarsb51214. Feel free to star, fork, and open issues if you encounter any problems or have suggestions!


---
**<p align="center">Generated by [ReadmeCodeGen](https://www.readmecodegen.com/)</p>**