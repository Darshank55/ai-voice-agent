AI Voice Agent Documentation

Overview
This AI Voice Agent is a multi-turn conversational system designed to handle sales-oriented voice interactions using Cohere for dialogue generation, Twilio for call handling, Deepgram for real-time transcription, and ElevenLabs for text-to-speech synthesis.

Technologies Used
- Call Handling: Twilio
- Speech-to-Text: Deepgram
- Conversational AI: Cohere
- Text-to-Speech: ElevenLabs
- Conversation Logging: JSON/Database storage
- UI Dashboard: React & Vite

Features
1. Call Handling
   - Supports both incoming and outgoing calls via Twilio.
   - Engages in human-like interactions with customers.
2. Speech-to-Text Processing
   - Converts spoken input to text using Deepgram.
   - Ensures low-latency transcription.
3. Conversational AI
   - Generates responses using Cohere AI.
   - Maintains conversation context dynamically.
4. Text-to-Speech Synthesis
   - Uses ElevenLabs for high-quality speech output.
5. Conversation Logging
   - Stores conversation data (transcripts, timestamps, metadata) in a structured format.
6. Sales-Oriented Dialogue Flow
   - Greets customers, asks open-ended questions, presents sales pitches, and handles objections.
7. UI Dashboard
   - Built using React & Vite for real-time conversation monitoring.

System Architecture
1. User Initiates Call: Twilio receives the call and routes it to the AI agent.
2. Speech-to-Text Processing: Deepgram transcribes the audio in real-time.
3. Conversational AI: The transcribed text is processed by Cohere, generating relevant responses.
4. Text-to-Speech Conversion: ElevenLabs converts the AI response into speech.
5. Response Sent to User: Twilio plays the synthesized voice to the caller.
6. Logging: The conversation data is stored for review.

API Usage
- Twilio: Call handling (incoming & outgoing)
- Deepgram: Speech recognition API
- Cohere: AI-generated response API
- ElevenLabs: TTS API

Deployment Steps
1. Clone the Repository:
   ```bash
   git clone https://github.com/your-repo/ai-voice-agent.git
   cd ai-voice-agent
   ```
2. Install Dependencies:
   ```bash
   pip install -r requirements.txt
   npm install (for UI)
   ```
3. Set Up Environment Variables** (add `.env` file):
   ```
   TWILIO_ACCOUNT_SID=your_sid
   TWILIO_AUTH_TOKEN=your_token
   DEEPGRAM_API_KEY=your_key
   COHERE_API_KEY=your_key
   ELEVENLABS_API_KEY=your_key
   ```
4. Run the Backend:
   ```bash
   python server.py
   ```
5. Run the UI:
   ```bash
   cd ui-dashboard
   npm run dev
   ```
6. Expose Server via Ngrok:
   ```bash
   ngrok http 5001

