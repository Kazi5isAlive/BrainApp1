# Audio Frequency Tuner

A sophisticated web-based audio frequency tuner with binaural beats generation, voice pattern matching, and real-time visualizations.

## Features

- **Binaural Beats Generator** - Create brain wave entrainment tones (Delta, Theta, Alpha, Beta, Gamma)
- **Voice Pattern Matcher** - Match your voice to target frequencies
- **Real-time Audio Analysis** - Visual frequency spectrum and waveform display
- **Sacred Geometry Visualizer** - Frequency-responsive geometric patterns
- **MP3 Player** - Play and analyze your own audio files
- **Advanced Audio Effects** - White noise, isochronic tones, frequency sweeping

## Quick Start

### Prerequisites
- Node.js 18+ installed on your system
- Modern web browser with microphone access

### Installation

1. **Download the project files** to your computer
2. **Open terminal/command prompt** in the project folder
3. **Install dependencies:**
   ```bash
   npm install
   ```
4. **Start the application:**
   ```bash
   npm run dev
   ```
5. **Open your browser** to `http://localhost:5000`

### Usage

1. **Allow microphone access** when prompted by your browser
2. **Choose a frequency range** from the sidebar (Delta: 0.5-4Hz, Theta: 4-8Hz, etc.)
3. **Start binaural beats** using the play button
4. **Adjust volume** and other settings in the control panel
5. **Watch real-time visualizations** as audio plays

### Production Build

To create a production build:
```bash
npm run build
npm run start
```

## Browser Support

- Chrome/Chromium (recommended)
- Firefox
- Safari
- Edge

**Note:** Microphone access is required for voice pattern matching features.

## Troubleshooting

- **No audio**: Check browser permissions for microphone access
- **Build errors**: Ensure Node.js 18+ is installed
- **Port conflicts**: Change port in package.json if 5000 is occupied

## Technical Details

- **Frontend**: React + TypeScript + Tailwind CSS
- **Audio Processing**: Web Audio API
- **Visualizations**: Canvas 2D rendering
- **Build System**: Vite + ESBuild