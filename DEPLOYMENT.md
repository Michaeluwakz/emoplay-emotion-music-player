# 🚀 Deployment Guide

## GitHub Pages (Recommended)

### Step 1: Enable GitHub Pages
1. Go to your repository settings
2. Scroll down to "Pages" section
3. Select "Deploy from a branch"
4. Choose "main" branch and "/ (root)" folder
5. Click "Save"

### Step 2: Update Spotify Redirect URI
1. Go to [Spotify Developer Dashboard](https://developer.spotify.com/dashboard)
2. Edit your app settings
3. Add your GitHub Pages URL to redirect URIs:
   - `https://yourusername.github.io/emoplay-emotion-music-player/`
4. Save changes

### Step 3: Update Code
Replace the redirect URI in your code:
```javascript
const SPOTIFY_REDIRECT_URI = 'https://yourusername.github.io/emoplay-emotion-music-player/';
```

## Netlify

### Step 1: Connect Repository
1. Go to [Netlify](https://netlify.com)
2. Click "New site from Git"
3. Connect your GitHub repository
4. Deploy settings:
   - Build command: `echo "No build needed"`
   - Publish directory: `.`

### Step 2: Update Spotify Settings
Add Netlify URL to Spotify redirect URIs:
- `https://your-app-name.netlify.app/`

## Vercel

### Step 1: Deploy
1. Go to [Vercel](https://vercel.com)
2. Import your GitHub repository
3. Deploy with default settings

### Step 2: Update Spotify Settings
Add Vercel URL to Spotify redirect URIs:
- `https://your-app-name.vercel.app/`

## Local Development

### Using Python
```bash
python -m http.server 3000
```

### Using Node.js
```bash
npm install
npm start
```

### Using Live Server
```bash
npm install -g live-server
live-server --port=3000
```

## Environment Variables

For production, consider using environment variables for sensitive data:

```javascript
const SPOTIFY_CLIENT_ID = process.env.SPOTIFY_CLIENT_ID || 'your-client-id';
```

## HTTPS Requirements

- Spotify API requires HTTPS in production
- GitHub Pages provides HTTPS automatically
- Netlify and Vercel provide HTTPS automatically
- For local development, use `localhost` or set up HTTPS

## Troubleshooting

### Common Issues
1. **CORS errors**: Make sure redirect URI matches exactly
2. **HTTPS required**: Use HTTPS in production
3. **Camera access**: Requires HTTPS or localhost
4. **Audio context**: Requires user interaction first

### Testing
1. Test on different browsers
2. Test on mobile devices
3. Verify Spotify integration works
4. Check camera permissions
