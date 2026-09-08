# iPhone XR Linux Server Simulator  
_A single‑page web app that mimics an iPhone XR interface while actually running on a lightweight ARM‑based Linux server._

## What It Does  

| Capability | Description |
|------------|-------------|
| **Boot sequence** | Shows a realistic, colour‑coded console log (OK/WARN/INFO) before handing off to the UI. |
| **iOS‑style home screen** | Glass‑morphism widgets (weather, calendar) and an app grid that looks like iOS 13+. |
| **Dock** | Persistent bottom dock with Phone, Safari, Messages and Music icons. |
| **Photos app** | Scrollable 3 × 4 grid of placeholder images; tap to open a full‑screen viewer. |
| **Phone app** | Dial‑pad UI with a mock call screen (shows “Calling …” then “Call Failed”). |
| **Messages app** | Chat list with avatars and bubble‑style conversation view. |
| **Safari app** | URL bar + “Go” button; displays a loading spinner and a fake 404 response. |
| **Spotify app** | Minimal music player with rotating album art, play/pause toggle and progress bar. |
| **About page** | Full‑screen overlay that explains the virtual hardware (A12 Bionic, 3 GB RAM) and VM constraints (2 CPU cores, 1 GB RAM). |
| **Swipe‑up‑to‑close** | Click‑and‑drag on the bottom bar dismisses the current app, reproducing iOS gesture behaviour. |
| **Pure vanilla stack** | Implemented entirely with HTML, CSS and native JavaScript—no external libraries or frameworks. |

## Where It Runs  

- **Runtime**: The UI runs in any modern browser (Chrome, Firefox, Safari, Edge) that supports ES6, CSS variables, `backdrop-filter`, and CSS animations.  
- **Server side**: The page can be served from a minimal static‑file host or directly from a **virtualized ARM Linux environment** (e.g., a Debian VM with an A12 Bionic‑class CPU). The VM provides the networking and HTTP service; the front‑end code executes client‑side in the browser.  

Because the project contains only static assets, the server can be as lightweight as a single‑core, 512 MiB configuration and still deliver a smooth experience.
