# Audio-Visual Cooking Assistant (VoiceChef-AI)

Lightweight assistant that combines audio streaming, vision overlays, and a Svelte front-end to help with step-by-step cooking guidance.

This repository contains:
- `frontend/` — Svelte app (UI, overlays, speaker/microphone controls)
- `server/` — Node.js server used for socket/stream handling
- `rhasspy/` — optional voice/NLU configuration for the Rhasspy assistant (prebuilt configs)
- Docker Compose manifests for running services via containers

## Prerequisites
- Node.js (v14+ recommended)
- npm or yarn
- Docker & Docker Compose (optional, for containerized runs)

## Quick start — Frontend (development)
Open a PowerShell terminal and run:

```powershell
cd frontend
npm install
npm run dev
```

The Svelte dev server (Rollup) should start and tell you which port it is serving (commonly `localhost:5000`).

## Quick start — Server (development)
Open a separate terminal and run:

```powershell
cd server
npm install
npm start
```

Adjust `server/src/index.js` configuration if you use a different port or require environment variables.

## Docker / Docker Compose
You can run the project with Docker Compose (root-level `docker-compose.yml` present):

```powershell
docker-compose up --build
```

This will build and start the services defined in the Compose files. See `docker-compose.override.yml` for local overrides.

## Notes on Development
- The app uses socket.io + socket.io-stream and RecordRTC for audio streaming from the browser.
- UI components live in `frontend/src/components/` (atoms/molecules/containers). Overlay click handlers dispatch events to the app logic.
- Accessibility (keyboard navigation, ARIA) is actively being improved in the frontend; if you see a11y warnings during builds, please review the Svelte warnings & the overlay components.

## Contributing
Feel free to open issues or PRs. When contributing, run the dev servers locally to verify UI and streaming behavior.

## License
This repository does not include a license file. Add one (e.g., MIT) if you plan to release the code publicly.

---
If you'd like, I can also:
- Commit the new `README.md` and create a git commit for you
- Add more detailed developer notes (scripts, ports, env vars)
- Run the frontend dev server to verify it starts (I can provide commands you can run locally)

*** End Patch
