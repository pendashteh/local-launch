# 🚀 Localhost Port Launcher

A sleek, modern browser homepage for web developers to quickly access local development servers.

## Features

### ⚡ Quick Launch
- Type any port number (1-65535) and hit Enter or click "Go"
- Auto-focuses on input field when page loads
- Input validation to ensure valid port numbers

### 📌 Common Port Presets
Pre-configured buttons for the most commonly used development ports:
- **3000** - React, Next.js
- **8080** - General web applications
- **5173** - Vite
- **4200** - Angular
- **8000** - Django
- **5000** - Flask
- **3001** - Backend services
- **9000** - API servers

### 📜 Recently Used Ports
- Automatically tracks the last 6 ports you've accessed
- Shows your most recent ports in a separate section
- One-click access to frequently used custom ports
- Clear history button to reset when needed
- Uses browser's localStorage to persist between sessions

## Installation

### Set as Browser Homepage

#### Chrome/Edge
1. Save the `localhost-launcher.html` file to your computer
2. Open Settings → Appearance → Show home button (enable)
3. Click "Enter custom web address"
4. Enter: `file:///path/to/localhost-launcher.html`
5. Or go to Settings → On startup → Open a specific page → Add the file path

#### Firefox
1. Save the `localhost-launcher.html` file
2. Open Settings → Home
3. Under "Homepage and new windows" select "Custom URLs"
4. Enter: `file:///path/to/localhost-launcher.html`

#### Safari
1. Save the file
2. Safari → Preferences → General
3. Set Homepage to: `file:///path/to/localhost-launcher.html`

### Alternative: Browser Extension
You can also use this as a new tab page by converting it into a browser extension (see browser extension documentation).

## Usage

### Launching a Port
1. **Quick Launch**: Type a port number and press Enter
2. **Preset Buttons**: Click any of the preset port buttons
3. **Recent Ports**: Click any recently used port from the history

### Managing History
- History is automatically saved when you use a port
- Click "Clear" button in the Recently Used section to reset history
- History persists across browser sessions
- Maximum of 6 recent ports are saved

## Customization

### Adding/Changing Preset Ports
Edit the HTML file and modify the preset buttons section:

```html
<button class="preset-btn" onclick="openLocalhost(YOUR_PORT)">
    <span class="preset-port">YOUR_PORT</span>
    <span class="preset-label">Your Label</span>
</button>
```

### Changing History Limit
In the JavaScript section, modify the `MAX_HISTORY` constant:

```javascript
const MAX_HISTORY = 6; // Change to your preferred number
```

### Styling
All styles are contained in the `<style>` section. You can customize:
- Colors (modify gradient values and color codes)
- Font sizes
- Spacing and layout
- Button styles

## Technical Details

- Pure HTML/CSS/JavaScript - no dependencies
- Uses **localStorage API** for history persistence
- **Works as a local HTML file** - no web server required!
- localStorage works with `file://` protocol in all modern browsers
- Opens ports in new tabs using `window.open()` with `_blank` target
- Responsive design works on mobile and desktop
- Modern gradient design with smooth animations
- Auto-focus on input for keyboard-first workflow

### How History Storage Works

The launcher uses the browser's **localStorage API** to persist your recently used ports:

- **localStorage** is a web API that stores key-value pairs in the browser
- Data persists even after closing the browser
- Works with local HTML files (`file://` protocol) - no server needed!
- Each browser has its own localStorage (Chrome, Firefox, etc. don't share data)
- Data is stored as JSON: `localStorage.setItem('portHistory', JSON.stringify(array))`
- Maximum 6 recent ports are kept automatically
- Completely private - stored only on your computer

## Browser Compatibility

- ✅ Chrome/Edge (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Opera (latest)

Requires localStorage support (available in all modern browsers).

## Privacy

All data is stored locally in your browser using localStorage. No data is sent to any external servers.

## License

Free to use and modify for personal and commercial projects.

## Tips

- Press `Tab` to quickly navigate between input and buttons
- Use keyboard shortcuts: Type port number → Enter
- Add this page to your bookmarks bar for quick access
- Customize preset ports based on your most common development stack

---

Made for developers, by developers. Happy coding! 💻
