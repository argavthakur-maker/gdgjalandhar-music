# Robot DJ · GDG Jalandhar

A browser-based, audio-first DJ experience with a 3D robot stage, a shuffled YouTube playlist, and a compact playback HUD. The player is built for the GDG Jalandhar community site and is deployed on GitHub Pages with the custom domain `dj.gdgjalandhar.com`.

## Features

- Shuffled playback from a configurable YouTube playlist.
- Automatic next-track playback and queue reshuffling when the queue ends.
- Play/pause, next track, mute, and volume controls.
- Keyboard shortcuts: **Space** to play/pause, **→** or **N** for next, and **M** to mute.
- Media Session integration for supported lock screens and hardware media keys.
- Animated 3D robot scene with playback progress and accent themes.
- Reduced-motion support for the scene's beat animation.

## Tech stack

- React 18 and TypeScript
- Vite
- Three.js, React Three Fiber, and Drei
- Framer Motion
- YouTube IFrame Player API

## Getting started

Use Node.js and npm, then run:

```bash
npm install
npm run dev
```

Vite prints the local development URL in the terminal.

## Production build

```bash
npm run build
npm run preview
```

The build command runs the TypeScript project checks before generating the static site in `dist/`.

## Playlist configuration

The default playlist is configured in `src/data/playlist.ts`. It must be public or unlisted, and its videos must allow embedding. To preview another playlist without editing source code, open the app with the `list` query parameter:

```text
?list=YOUR_YOUTUBE_PLAYLIST_ID
```

For example, append that query string to the local or deployed site URL. The player also reports an error if the playlist cannot be loaded or several tracks in a row cannot be embedded.

## Deployment

The project is configured for a root-path static deployment and the custom domain is managed through the repository's `CNAME` file. Build output is generated with `npm run build`; do not commit the generated `dist/` directory unless the deployment workflow explicitly requires it.

## License

See the repository's license file for usage and redistribution terms.
