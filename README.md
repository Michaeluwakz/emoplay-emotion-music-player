# 🎵 EmoPlay - Emotion-Based Music Player

A cutting-edge web application that detects your emotions through facial recognition and suggests personalized music recommendations using Spotify's API. Experience music that truly understands how you feel!

![EmoPlay Demo](https://img.shields.io/badge/Status-Live-brightgreen) ![Spotify](https://img.shields.io/badge/Spotify-API-1DB954) ![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow) ![Web Audio](https://img.shields.io/badge/Web%20Audio-API-orange)

## ✨ Features

### 🎭 Emotion Detection
- **Real-time facial emotion recognition** using TensorFlow.js
- **6 emotion categories**: Happy, Sad, Angry, Surprised, Fearful, Neutral
- **Live camera feed** with emotion overlay visualization
- **Confidence scoring** for emotion detection accuracy

### 🎶 Smart Music Recommendations
- **Spotify API integration** for real music recommendations
- **Emotion-to-genre mapping** for personalized suggestions
- **Audio features matching** (valence, energy, danceability)
- **Real album art** and track information display

### 🔊 Audio Playback
- **Spotify Web Playback SDK** for premium music streaming
- **Fallback audio system** with emotion-based tones
- **Web Audio API** for browser-compatible sound generation
- **Play/pause controls** with progress tracking

### 🎨 Modern UI/UX
- **Responsive design** that works on all devices
- **Dark theme** with vibrant accent colors
- **Smooth animations** and transitions
- **Real-time status indicators** and debug information

## 🚀 Quick Start

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Camera access for emotion detection
- Spotify account (Premium required for full music playback)

### Installation

1. **Clone or download** this repository
2. **Open `Index.html`** in your web browser
3. **Allow camera access** when prompted
4. **Connect to Spotify** for music recommendations

```bash
# If using a local server (recommended)
python -m http.server 3000
# or
npx serve .
```

## 🔧 Spotify Setup

### Step 1: Create Spotify App
1. Go to [Spotify Developer Dashboard](https://developer.spotify.com/dashboard)
2. Click "Create App"
3. Fill in app details:
   - **App name**: EmoPlay
   - **App description**: Emotion-based music player
   - **Website**: Your domain or localhost
   - **Redirect URI**: `http://localhost:3000` (or your domain)

### Step 2: Configure Redirect URIs
Add these redirect URIs to your Spotify app settings:
- `http://localhost:3000`
- `http://localhost:3000/`
- `file:///` (for local file access)

### Step 3: Get Client ID
1. Copy your **Client ID** from the app settings
2. Replace `YOUR_SPOTIFY_CLIENT_ID` in the code with your actual Client ID
3. Save the file

### Step 4: Test Connection
1. Click "Connect Spotify" button
2. Authorize the app with your Spotify account
3. Check the debug panel for connection status

## 🎮 How to Use

### Basic Usage
1. **Start Detection**: Click "Start Detection" to begin emotion recognition
2. **Allow Camera**: Grant camera permissions when prompted
3. **Connect Spotify**: Click "Connect Spotify" for music recommendations
4. **Play Music**: Click the play button to start audio playback

### Advanced Features
- **Test Audio**: Click "Test Audio" to verify browser audio support
- **Debug Info**: Check the debug panel for system status
- **Manual Token**: Use "Manual Token Input" if automatic auth fails

## 🎵 Emotion Mapping

| Emotion | Music Genres | Audio Features | Tone Frequency |
|---------|-------------|----------------|----------------|
| 😊 Happy | Pop, Dance, Upbeat | High valence, energy | C5 (523.25 Hz) |
| 😢 Sad | Blues, Indie, Folk | Low valence, energy | C4 (261.63 Hz) |
| 😠 Angry | Rock, Metal, Punk | High energy, low valence | A5 (880.00 Hz) |
| 😲 Surprised | Experimental, Electronic | Medium valence, energy | E5 (659.25 Hz) |
| 😨 Fearful | Ambient, Dark Ambient | Low valence, energy | A3 (220.00 Hz) |
| 😐 Neutral | Ambient, Classical, Jazz | Medium valence, energy | A4 (440.00 Hz) |

## 🔧 Technical Details

### Technologies Used
- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **AI/ML**: TensorFlow.js, BlazeFace, Face Landmarks Detection
- **Audio**: Web Audio API, Spotify Web Playback SDK
- **APIs**: Spotify Web API, Spotify Recommendations API
- **Styling**: CSS Grid, Flexbox, CSS Variables

### Browser Compatibility
- ✅ Chrome 80+
- ✅ Firefox 75+
- ✅ Safari 13+
- ✅ Edge 80+

### Audio Requirements
- **Spotify Premium** for full music playback
- **Web Audio API** support for fallback tones
- **HTTPS or localhost** for secure context

## 🐛 Troubleshooting

### Common Issues

#### "No Sound" Problem
- **Check volume**: Ensure system and browser volume are up
- **Test Audio**: Click "Test Audio" button to verify audio support
- **Browser permissions**: Some browsers block audio until user interaction
- **HTTPS requirement**: Use HTTPS or localhost for audio context

#### "INVALID_CLIENT" Error
- **Check redirect URI**: Must match exactly in Spotify app settings
- **Common URIs**: `http://localhost:3000`, `file:///`
- **Console logs**: Check browser console for exact URI being used

#### "No Token" Error
- **Spotify Premium**: Required for Web Playback SDK
- **Manual Token**: Use "Manual Token Input" as fallback
- **Token Expiry**: Tokens expire after 1 hour, re-authenticate

#### Camera Not Working
- **Permissions**: Allow camera access when prompted
- **HTTPS**: Camera requires secure context
- **Browser support**: Ensure browser supports getUserMedia API

### Debug Information
The debug panel shows real-time status of:
- Spotify SDK loading
- Access token status
- Device ID readiness
- Player initialization

## 📱 Mobile Support

### Responsive Design
- **Mobile-first** approach
- **Touch-friendly** controls
- **Adaptive layout** for different screen sizes
- **Camera access** on mobile devices

### Limitations
- **Spotify Web Playback SDK** has limited mobile support
- **Fallback audio** works on all devices
- **Camera quality** may vary on mobile

## 🔒 Privacy & Security

### Data Handling
- **No data storage**: Emotions are processed locally
- **No tracking**: No personal data is collected
- **Local processing**: All AI processing happens in browser
- **Secure tokens**: Spotify tokens stored locally only

### Permissions
- **Camera**: Required for emotion detection
- **Audio**: Required for music playback
- **Local Storage**: For Spotify token persistence

## 🚀 Future Enhancements

### Planned Features
- [ ] **Playlist creation** based on emotion history
- [ ] **Mood tracking** over time
- [ ] **Social sharing** of emotion-based playlists
- [ ] **Voice commands** for hands-free control
- [ ] **Multiple emotion detection** (detecting multiple people)
- [ ] **Custom emotion mappings** (user-defined genres)

### Technical Improvements
- [ ] **PWA support** for offline functionality
- [ ] **WebRTC** for better camera handling
- [ ] **Machine learning** model improvements
- [ ] **Performance optimizations** for mobile

## 🤝 Contributing

### Development Setup
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

### Code Style
- **ES6+** JavaScript
- **CSS Grid/Flexbox** for layout
- **Semantic HTML** structure
- **Accessibility** considerations

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Spotify** for the amazing Web API and Playback SDK
- **TensorFlow.js** team for the machine learning capabilities
- **Web Audio API** for browser audio support
- **Font Awesome** for the beautiful icons
- **Google Fonts** for the Inter font family

## 📞 Support

### Getting Help
- **Issues**: Check the debug panel for error details
- **Console**: Open browser console (F12) for detailed logs
- **Documentation**: Refer to this README for setup instructions
- **Spotify API**: [Official Documentation](https://developer.spotify.com/documentation/)
