# AI Medical Assistant with Google Text-to-Speech

A sophisticated AI-powered medical chatbot with high-quality voice synthesis using Google Cloud Text-to-Speech API.

## 🎯 Features

### Core Functionality
- **AI Medical Consultation**: Get professional medical advice powered by Google Gemini
- **Multilingual Support**: Full Telugu and English language support
- **Image Analysis**: Upload medical images for AI-powered analysis
- **Voice Input**: Speech-to-text for hands-free interaction
- **Premium Voice Output**: Google Cloud Text-to-Speech integration

### Voice Capabilities
- **Google Cloud TTS**: High-quality neural voices for natural speech
- **English Voice**: Professional Indian English voice (en-IN-Wavenet-D)
- **Direct API Integration**: Uses Google TTS API directly for optimal performance
- **Audio Caching**: Efficient audio caching for improved performance
- **Real-time Status**: Live voice synthesis status indicators

### Medical Features
- **Health Context Detection**: Automatically detects health-related queries
- **Medical Disclaimers**: Appropriate medical disclaimers for health advice
- **Emergency Detection**: Identifies emergency symptoms and provides warnings
- **Professional Responses**: Medical-grade responses with proper context

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ 
- Google Cloud Text-to-Speech API key

### Installation

1. **Clone and Install**
   ```bash
   git clone <repository-url>
   cd ai-medical-assistant
   npm install
   ```

2. **Start Development**
   ```bash
   npm run dev
   ```

The application will start on `http://localhost:5173`

## 🔧 Configuration

### API Keys

The application uses the following API keys (configured in the source code):

- **Google Gemini AI**: `AIzaSyDXf4W88CpdbzRW_NSmR4d5wNWU2UThJ6Y`
- **Google Text-to-Speech**: `AIzaSyDXf4W88CpdbzRW_NSmR4d5wNWU2UThJ6Y`

### Voice Configuration

**English Voice:**
- Voice: `en-IN-Wavenet-D` (Indian English Male)
- Encoding: `MP3`
- Language: `en-IN`

## 🎤 Voice System Architecture

### Direct Google TTS Integration

The application uses a direct integration with Google Cloud Text-to-Speech API:

1. **Text Processing**: Cleans and prepares text for optimal voice synthesis
2. **API Request**: Sends request directly to Google TTS API with API key
3. **Audio Generation**: Receives base64-encoded MP3 audio
4. **Playback**: Converts to audio URL and plays using HTML5 Audio API
5. **Caching**: Caches audio for repeated phrases to improve performance

### Voice Features

- **Real-time Status**: Live indicators for voice synthesis progress
- **Quality Indicators**: Visual badges showing voice quality and provider
- **Error Handling**: Graceful error handling with user feedback
- **Automatic Playback**: Bot responses are automatically spoken
- **Manual Replay**: Users can replay any bot message

## 🏥 Medical Features

### Health Detection
- Automatic detection of health-related queries
- Context-aware medical responses
- Emergency symptom identification
- Appropriate medical disclaimers

### Supported Medical Topics
- Symptoms and diagnosis
- Medications and treatments
- Health conditions
- Preventive care
- Emergency situations

## 📱 Voice Integration

### Automatic Voice Responses
Every chatbot reply is automatically converted to speech using:

```javascript
// Example usage
const result = await speakText("Your medical advice here");
if (result.success) {
  console.log(`Spoken using: ${result.voiceUsed}`);
}
```

### Voice Controls
- **Voice Toggle**: Enable/disable automatic voice responses
- **Manual Replay**: Click voice button on any bot message
- **Status Indicators**: Real-time voice synthesis status

## 🔒 Security

- API keys are used directly in frontend (suitable for demo/development)
- Input validation and sanitization
- Error handling for API failures
- Rate limiting handled by Google's API quotas

## 🚀 Deployment

### Frontend-Only Deployment
Since this uses direct API integration, you only need to deploy the frontend:

```bash
npm run build
# Deploy the dist/ folder to your hosting provider
```

### Supported Platforms
- Netlify
- Vercel
- GitHub Pages
- Any static hosting provider

## 🛠️ Development

### Project Structure
```
src/
├── components/          # React components with voice integration
├── services/           # API services
│   ├── api.ts         # Gemini AI integration
│   └── directTTS.ts   # Direct Google TTS integration
├── utils/             # Utility functions
└── types/             # TypeScript types
```

### Available Scripts
- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run lint` - Run ESLint
- `npm run preview` - Preview production build

## 🎵 Voice Quality

| Feature | Google TTS | Browser TTS |
|---------|------------|-------------|
| Quality | High | Medium |
| Naturalness | Excellent | Good |
| Medical Terms | Excellent | Fair |
| Offline | No | Yes |
| Cost | API Usage | Free |
| Latency | Low | Instant |

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🆘 Support

For issues and questions:
1. Check the troubleshooting section
2. Review Google Cloud TTS documentation
3. Open an issue on GitHub

## 🔍 Troubleshooting

### Common Issues

**Voice Not Working**
- Check browser console for API errors
- Verify API key is valid and has TTS permissions
- Ensure internet connection is stable
- Try refreshing the page

**API Quota Exceeded**
- Google TTS has usage limits
- Monitor your API usage in Google Cloud Console
- Consider implementing usage limits in production

**Audio Playback Issues**
- Check browser audio permissions
- Verify audio output device is working
- Try different browsers (Chrome recommended)

### Browser Compatibility

- **Chrome**: Full support
- **Firefox**: Full support
- **Safari**: Full support
- **Edge**: Full support
- **Mobile**: Supported on modern mobile browsers

### Performance Tips

- Audio caching reduces API calls
- Clean text processing improves voice quality
- Error handling ensures graceful degradation
- Status indicators provide user feedback#   p r o j e c t - 1  
 