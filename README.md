# Intelligent Voice Customer Service Assistant

An AI customer service assistant based on voice interaction, capable of real-time voice conversations to help handle customer inquiries and generate sales leads.

## Features

- **Automatic Speech Recognition (ASR)**: Uses OpenAI Whisper API to convert speech to text
- **Natural Language Processing**: Processes conversations using LangChain and OpenAI GPT models
- **Text-to-Speech (TTS)**: Converts AI responses to voice output
- **Multi-mode Support**: Supports both customer service and sales lead generation modes
- **Conversation Analysis**: Analyzes conversation content and extracts key information
- **User-friendly Interface**: Intuitive user interface built with Streamlit

## Installation

### 1. Clone Repository

```bash
git clone <repository-url>
cd <repository-directory>
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Configure Environment Variables

Create a `.env` file and add the following content:

```
OPENAI_API_KEY=your_openai_api_key_here
LLM_MODEL=gpt-3.5-turbo
SAMPLE_RATE=16000
```

Replace `your_openai_api_key_here` with your OpenAI API key.

## Usage

### Launch Application

```bash
streamlit run app.py
```

### Using the Interface

1. **Voice Interaction**:
   - Click the "Start Recording" button for voice input
   - Or upload an audio file for processing

2. **Text Interaction**:
   - Enter questions in the text input box
   - The system will generate text responses and provide voice output

3. **Conversation Analysis**:
   - Click the "Analyze Conversation" button after the dialogue
   - The system will analyze the conversation content and provide a summary

### Settings

The following settings can be adjusted in the sidebar:

- **Recording Duration**: Adjust the duration of recording
- **Mode Selection**: Switch between customer service mode or sales lead generation mode
- **Clear Conversation History**: Reset the current conversation

## System Requirements

- Python 3.8+
- Valid OpenAI API key
- Microphone (for voice input)
- Speakers (for voice output)

## Technology Stack

- **Streamlit**: User interface
- **OpenAI Whisper**: Speech recognition
- **LangChain**: LLM interaction framework
- **gTTS**: Text-to-speech
- **Matplotlib**: Audio visualization
- **SoundDevice & SoundFile**: Audio processing

## Important Notes

- Ensure your OpenAI API key has sufficient quota
- Voice recognition and generation may require a stable network connection
- Recording function requires browser microphone access permission

## Troubleshooting

### OpenAI API Quota Insufficient Error

If you encounter the following error:
```
Error code: 429 - {'error': {'message': 'You exceeded your current quota, please check your plan and billing details.', 'type': 'insufficient_quota', 'param': None, 'code': 'insufficient_quota'}}
```

This indicates that your OpenAI API quota has been exhausted. Here are the solutions:

1. **Add Payment Method**:
   - Log in to your [OpenAI account](https://platform.openai.com/account/billing/overview)
   - Add a valid payment method
   - Set usage limits to control spending

2. **Get Free Credits**:
   - Newly registered OpenAI API users typically receive some free credits (usually $5 or $18)
   - These credits are valid for the first three months after registration
   - Register new account: [OpenAI API Registration](https://platform.openai.com/signup)

3. **Use Alternative Models**:
   - Modify the `LLM_MODEL` setting in the `.env` file to use lower-cost models
   - For example, use `gpt-3.5-turbo` instead of `gpt-4`

4. **Local Alternatives**:
   - Consider using locally run open-source models, such as the local version of Whisper for speech recognition
   - Modify code to support local models (requires additional development)

### Other Common Issues

- **Microphone Access Denied**: Ensure you have granted browser microphone access permission
- **Audio Quality Issues**: Try adjusting recording settings or use an external microphone
- **Response Delays**: Check your network connection or increase timeout settings

## License

[MIT License](LICENSE)