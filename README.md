# 🎓 Teaching Assistant AI
### Interactive Voice-Based AI Tutor for Children

<div align="center">

![Python](https://img.shields.io/badge/Python-3.8+-yellow?style=for-the-badge&logo=python)
![OpenAI](https://img.shields.io/badge/OpenAI-GPT--3.5-green?style=for-the-badge&logo=openai)
![AssemblyAI](https://img.shields.io/badge/AssemblyAI-Speech--to--Text-blue?style=for-the-badge&logo=assemblyai)
![ElevenLabs](https://img.shields.io/badge/ElevenLabs-Text--to--Speech-orange?style=for-the-badge&logo=elevenlabs)

*A real-time, voice-interactive AI companion designed to make learning fun and accessible for children.*

[🔗 Repository](https://github.com/chiragkhachane/Teaching_Assistant_AI) • [🐛 Report Issue](https://github.com/chiragkhachane/Teaching_Assistant_AI/issues)

</div>

## 🌟 Overview

**Teaching Assistant AI** is an innovative educational tool that leverages cutting-edge AI technologies to create a real-time, voice-based tutoring experience. Designed specifically for children, this AI assistant acts as a kind, patient, and knowledgeable teacher who can explain concepts in simple terms, conduct quizzes, and engage in meaningful educational conversations.

By combining real-time speech recognition, advanced language modeling, and natural-sounding voice synthesis, the application provides a seamless "talk-to-learn" interface that mimics a natural conversation with a human tutor.

## ✨ Key Features

- **🗣️ Real-Time Voice Interaction**: Seamlessly listens to the user's voice and responds with natural speech, creating a hands-free learning environment.
- **🤖 Child-Friendly Persona**: The AI is prompted to be kind, patient, and age-appropriate, ensuring a safe and encouraging learning atmosphere.
- **📚 Educational Quizzes & Passages**: Capable of generating reading passages, asking comprehension questions, and keeping track of scores.
- **🧠 Context-Aware Conversations**: Maintains conversation history to understand context and provide relevant follow-up responses.
- **🛡️ Safe Content Policy**: Strictly filtered to ensure all interactions are suitable for children, with no adult content.

## 🏗️ System Architecture

The application follows a cyclical data flow to enable real-time interaction:

```mermaid
graph TD
    User[User (Child)] -->|Voice Input| Mic[Microphone Stream]
    Mic -->|Audio Stream| AAI[AssemblyAI]
    AAI -->|Real-time Transcription| Text[Text Input]
    Text -->|Prompt + Context| GPT[OpenAI GPT-3.5]
    GPT -->|AI Response Text| EL[ElevenLabs]
    EL -->|Synthesized Audio| Speaker[Speaker Output]
    Speaker --> User
```

1.  **Speech-to-Text (STT)**: **AssemblyAI** processes the microphone stream in real-time to convert speech into text.
2.  **Intelligence (LLM)**: **OpenAI's GPT-3.5-turbo** processes the transcribed text, generates an educational response based on the system persona, and maintains conversation context.
3.  **Text-to-Speech (TTS)**: **ElevenLabs** converts the AI's text response into a high-quality, natural-sounding voice (Voice: "Daniel").

## 🛠️ Technology Stack

| Component | Technology | Purpose |
|-----------|------------|---------|
| **Language** | Python | Core application logic |
| **Speech-to-Text** | AssemblyAI SDK | Real-time audio transcription |
| **LLM / Intelligence** | OpenAI API | Natural language understanding and generation |
| **Text-to-Speech** | ElevenLabs API | High-fidelity voice synthesis |
| **Environment** | Python-Dotenv | Secure configuration management |

## 🚀 Getting Started

### Prerequisites

- Python 3.8 or higher
- A working microphone and speaker
- API Keys for:
    - [AssemblyAI](https://www.assemblyai.com/)
    - [OpenAI](https://openai.com/)
    - [ElevenLabs](https://elevenlabs.io/)

### Installation

1.  **Clone the repository**
    ```bash
    git clone https://github.com/chiragkhachane/Teaching_Assistant_AI.git
    cd Teaching_Assistant_AI
    ```

2.  **Install dependencies**
    ```bash
    pip install assemblyai elevenlabs openai python-dotenv
    ```

3.  **Configure Environment Variables**
    Create a `.env` file in the root directory and add your API keys:
    ```env
    ASSEMBLYAI_API_KEY=your_assemblyai_key
    OPENAI_API_KEY=your_openai_key
    ELEVENLABS_API_KEY_2=your_elevenlabs_key
    ```
    *> **Note**: The code specifically looks for `ELEVENLABS_API_KEY_2`.*

### Usage

1.  **Run the application**
    ```bash
    python main.py
    ```

2.  **Start Learning!**
    - The assistant will greet you with: *"Hi! How can I help you?"*
    - Speak clearly into your microphone.
    - The AI will transcribe your speech, think for a moment, and respond verbally.
    - You can ask for a story, a quiz, or an explanation of a topic!

## 📝 Configuration

The AI's behavior is defined by the system prompt in `main.py`. You can modify the `AI_Assistant` class initialization to change the persona:

```python
self.full_transcript = [
    {
        "role": "system", 
        "content": "You are a Teaching AI Assistant Teacher for 5 year old children... Explain in very simple terms..."
    }
]
```

## 🤝 Contributing

Contributions are welcome! If you have ideas for new features, better prompting strategies, or UI improvements, feel free to fork the repository and submit a pull request.

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- **AssemblyAI** for their robust real-time transcription API.
- **OpenAI** for the powerful language models that drive the intelligence.
- **ElevenLabs** for providing lifelike voice synthesis.

---

<div align="center">

**Empowering the next generation of learners through AI.** 🚀

[📧 Contact Developer](mailto:chiragkhachane@gmail.com)

</div>
