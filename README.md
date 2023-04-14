# ChatGPT Voice Assistant - Hey Nova
Introducing a voice assistant powered by GPT, which runs locally on your machine and allows you to converse with it as if you were interacting with Google Assistant or Alexa. The best part? It's completely free of charge, as it leverages your personal OpenAI account.

[![Python version](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This is an open-source repository for a voice-controlled chatbot called Nova. It utilizes Google's Speech Recognition API for speech-to-text and [GPT-3 unofficial API](https://github.com/acheong08/ChatGPT) for generating responses. The chatbot can be controlled using voice commands and generates audio responses. 

Once the assistant is triggered with the keyword **"Hello Nova"**, it starts listening for user input. The assistant will continue to listen and respond in a conversational manner until the user says **"Bye Nova"**. The assistant is capable of answering questions and generating coherent dialogues as if you were texting with ChatGPT.

The chatbot was built using several libraries. These include:

- `SpeechRecognition`: used for speech recognition of the user's input
- `gtts`: used for text-to-speech conversion of the chatbot's responses
- `revChatGPT`: used for generating responses using GPT-3
- `pydub` and `simpleaudio`: used for playing audio responses

The chatbot is available in English (default) and Spanish.

## How to Install

Before installing, make sure you have the following packages installed:

```bash
brew install pyaudio ffmpeg # (or apt-get in Linux)
pip install SpeechRecognition gtts revChatGPT pydub simpleaudio
```

Next, clone the repository and navigate to the project directory:

```bash
git clone https://github.com/yourusername/nova-chatbot.git
cd nova-chatbot
```

You also need to get the `accessToken` by logging into your OpenAI account, accessing the following link https://chat.openai.com/api/auth/session, copy the access token, and save it in the root directory as `credentials.json`. 

## How to Use

You can control the chatbot using voice commands. To start the chatbot with default settings (English language and 1.25 speed multiplier), run the following command:

```bash
python app.py
```

To specify the language and speed multiplier, use the `-l` and `-s` options and provide the corresponding values:

```bash
python app.py -l es -s 1.0
```

To use a different name for the chatbot assistant, use the `-a` option:

```bash
python app.py -a Lumi
```

The options can also be combined:

```bash
python app.py -l en -s 1.25 -a Nova
```

The chatbot can be activated by saying "Hello `<assistant-name>`" and will continue to listen and respond until the user says "Bye `<assistant-name>`". 

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.