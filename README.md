# 🤖 Baymax AI - Personal Voice Assistant

<div align="center">

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![LiveKit](https://img.shields.io/badge/LiveKit-Agents-green.svg)
![Google AI](https://img.shields.io/badge/Google-Gemini-orange.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

*Your personal AI companion inspired by Iron Man's butler - classy, sarcastic, and incredibly helpful*

</div>

## 📋 Overview

Baymax AI is an intelligent voice assistant powered by Google's Gemini Realtime model and LiveKit's real-time communication framework. Like a sophisticated butler, Baymax provides personalized assistance with a touch of class and wit, capable of performing web searches, fetching weather information, and engaging in natural conversations.

## ✨ Key Features

- 🎙️ **Real-time Voice Interaction** - Seamless voice communication using LiveKit
- 🧠 **Advanced AI** - Powered by Google's Gemini Realtime model with "Charon" voice
- 🌦️ **Weather Integration** - Get current weather for any city
- 🔍 **Web Search** - Perform web searches using DuckDuckGo
- 🎭 **Personality** - Classy butler persona with a sarcastic edge
- 🎥 **Video Support** - Includes video streaming capabilities
- 🔇 **Noise Cancellation** - Built-in enhanced noise cancellation (BVC)

## 🛠️ Tech Stack

- **AI Framework**: Google Gemini Realtime Model
- **Communication**: LiveKit Agents
- **Voice**: Custom "Charon" voice profile
- **Search**: DuckDuckGo API via langchain_community
- **Weather**: wttr.in API
- **Environment**: Python 3.8+

## 📦 Installation

### Prerequisites

- Python 3.8 or higher
- LiveKit Cloud account (or self-hosted LiveKit server)
- Google API credentials

### Setup

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/baymax-ai.git
cd baymax-ai/Baymax-AI-main
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **Configure environment variables**

Create a `.env` file in the project root:
```env
LIVEKIT_URL=your_livekit_url
LIVEKIT_API_KEY=your_api_key
LIVEKIT_API_SECRET=your_api_secret
GOOGLE_API_KEY=your_google_api_key
```

4. **Run the agent**
```bash
python agent.py
```

## 🎯 Usage

### Starting Baymax

```bash
python agent.py
```

Baymax will greet you with:
> "Hi my name is Baymax, Your personal companion. How may I assist you today?"

### Available Commands

- **Weather Queries**: "What's the weather in London?"
- **Web Searches**: "Search for the latest tech news"
- **General Assistance**: Ask anything and Baymax will help with a touch of sarcasm

### Example Interactions

```
User: "Hi, can you check the weather for me?"
Baymax: "Of course sir, as you wish. I will now fetch the weather information for you."

User: "Search for Python tutorials"
Baymax: "Roger Boss. I've found some excellent Python tutorials for you."
```

## 📁 Project Structure

```
Baymax-AI-main/
├── agent.py           # Main agent entry point
├── prompts.py         # Agent personality and instructions
├── tools.py           # Helper tools (weather, search, news)
├── requirements.txt   # Python dependencies
├── Livekit-API.txt   # LiveKit API documentation
└── __pycache__/      # Python cache files
```

## 🔧 Configuration

### Agent Settings

Modify `agent.py` to adjust:
- **Temperature**: Controls response creativity (default: 0.8)
- **Voice**: Change voice profile (default: "Charon")
- **Video**: Enable/disable video support
- **Noise Cancellation**: Configure BVC settings

### Personality Customization

Edit `prompts.py` to customize:
- Agent persona and speaking style
- Response patterns
- Initial greeting message

## 🛡️ Available Tools

### 1. Weather Tool
Fetches current weather for any city using wttr.in API.

```python
@function_tool()
async def get_weather(context: RunContext, city: str) -> str
```

### 2. Web Search Tool
Performs web searches using DuckDuckGo.

```python
@function_tool()
async def search_web(context: RunContext, query: str) -> str
```

### 3. News Tool (Optional)
Fetches latest news for a given topic.

```python
@function_tool()
async def get_latest_news(context: RunContext, topic: str) -> str
```

## 📚 Dependencies

```
livekit-agents                    # Core agent framework
livekit-plugins-google            # Google AI integration
livekit-plugins-noise-cancellation # Audio enhancement
livekit-plugins-silero            # Voice activity detection
duckduckgo-search                 # Web search capability
langchain_community               # Search tools
python-dotenv                     # Environment management
requests                          # HTTP requests
```

## 🚀 Deployment

### LiveKit Cloud
1. Sign up at [LiveKit Cloud](https://livekit.io/)
2. Create a new project
3. Copy API credentials to `.env`
4. Deploy using LiveKit's agent deployment tools

### Self-Hosted
1. Set up your own LiveKit server
2. Configure `LIVEKIT_URL` to point to your server
3. Run the agent on your infrastructure

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- Inspired by Big Hero 6 Baymax and Iron Man's AI assistant
- Built with [LiveKit](https://livekit.io/)
- Powered by [Google Gemini](https://deepmind.google/technologies/gemini/)
- Search powered by [DuckDuckGo](https://duckduckgo.com/)

## 📞 Support

For issues and questions:
- Open an issue on GitHub
- Check LiveKit documentation
- Review Google Gemini API docs

## 🔮 Future Enhancements

- [ ] Memory integration with mem0ai
- [ ] Additional voice profiles
- [ ] Custom wake word detection
- [ ] Integration with smart home devices
- [ ] Multi-language support
- [ ] Enhanced personality modes

---

<div align="center">

**Made with ❤️ by your friendly neighborhood developer**

*"Will do, Sir"* - Baymax

</div>
