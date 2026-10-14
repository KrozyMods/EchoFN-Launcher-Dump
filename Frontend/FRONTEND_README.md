# Echo Launcher Frontend

## Extraction Status

Successfully extracted all frontend assets from the Tauri 2.x executable using `tauri-dumper`.

## File Structure

### Root Files
- `index.html` - Main HTML entry point
- `app.js` - Main application logic (129 KB)
- `ui.css` - Main stylesheet (170 KB)
- `__packclamp.html` - Pack clamp HTML
- `data-store.js` - Data store management
- `tauri-bridge.js` - Tauri bridge for IPC communication

### Tab Components
- `tab-main.js` - Main tab
- `tab-news.js` - News tab
- `tab-builds.js` - Builds tab
- `tab-shop.js` - Shop tab
- `tab-servers.js` - Servers tab
- `tab-mods.js` - Mods tab
- `tab-profile.js` - Profile tab
- `tab-settings.js` - Settings tab
- `settings-rewards.js` - Settings rewards

### Other Components
- `onboarding.js` - Onboarding flow
- `side-rail.js` - Side rail navigation
- `actions.js` - Action handlers
- `themes.js` - Theme management
- `music-packs.js` - Music pack management

### Assets (`/assets/`)
- `config.json` - Configuration file with backend URL
- `FortniteLauncher.exe` - Embedded Fortnite launcher
- `fonts/` - Font files (Poppins, Burbank, JetBrains Mono, Material Symbols)
- `images/` - Images (backgrounds, logos, splash screens)

## Configuration

`assets/config.json`:
```json
{
    "backendUrl": "https://api.echofn.org"
}
```

## How to Rebuild

### Prerequisites
- Node.js (for frontend development)
- Tauri CLI
- Rust toolchain (for Tauri backend)

### Steps
1. Edit the JavaScript/CSS files as needed
2. Update `assets/config.json` if changing backend URL
3. Use Tauri CLI to rebuild:
   ```bash
   tauri build
   ```

### Modifying Assets
- Replace files in `assets/` directory
- Ensure relative paths are maintained
- Test changes before building

## Notes

- The frontend uses vanilla JavaScript (no framework detected)
- Uses Tauri IPC bridge for backend communication
- All assets are Brotli-compressed in the compiled binary
- The extracted files are decompressed and ready to edit
