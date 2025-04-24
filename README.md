# Google ADK Speaker Agent with ElevenLabs

This project demonstrates a Text-to-Speech (TTS) Speaker agent built using Google's Agent Development Kit (ADK) and ElevenLabs' MCP server.

## Overview

The speaker agent connects to the ElevenLabs MCP server via `uvx` to provide text-to-speech capabilities. It's built using:
- [Google ADK (Agent Development Kit)](https://github.com/google/adk-python)
- [ElevenLabs MCP Server](https://github.com/elevenlabs/elevenlabs-mcp)
- Python 3.11+

## Prerequisites

- Python 3.11 or higher
- ElevenLabs API key
- Google Gemini API key
- Google ADK installed

## Setup

1. Clone the repository:
```bash
git clone <your-repo-url>
cd google-elevnlabs-mcp
```

2. Create and activate a virtual environment:
```bash
python3.11 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Create a `.env` file in the root directory with your ElevenLabs and Gemini API keys:
```bash
ELEVENLABS_API_KEY=your_api_key_here
GOOGLE_API_KEY = your_api_key_here

```

## Running the Agent

1. Make sure your virtual environment is activated:
```bash
source venv/bin/activate
```

2. Navigate to the agents directory:
```bash
cd agents
```

3. Run the agent using ADK. You can only run async agents via the web client:
```bash
adk web
```

The agent will connect to the ElevenLabs MCP server and be ready to process text-to-speech requests (along with the other serviceable tools in the MCP server)

## Project Structure

```
google-adk-sample/
├── agents/
│   └── speaker/
│       ├── agent.py        # Main agent implementation
│       └── __init__.py
├── .env                    # Environment variables
└── requirements.txt        # Project dependencies
```

## Troubleshooting

If you encounter any issues:
1. Ensure your virtual environment is activated
2. Verify your API keys are correctly set in the `.env` file
3. Check that all dependencies are installed correctly
4. Make sure you're running the command from the correct directory

## Additional Resources

- [Google ADK Documentation](https://google.github.io/adk-docs/)
- [ElevenLabs Documentation](https://docs.elevenlabs.io/)
- [uvx Documentation](https://github.com/google/uvx)


