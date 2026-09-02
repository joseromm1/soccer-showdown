# ⚽ Soccer Showdown

A fast, arcade-style 2D soccer game built with [Phaser 3](https://phaser.io/). Play against a bot, share the keyboard with a friend locally, or challenge someone online over a peer-to-peer connection (no server required, powered by [PeerJS](https://peerjs.com/)).

## Play it

Once deployed with GitHub Pages (see below), just open the URL in a browser — no install needed.

To run it locally, you need a local web server (opening `index.html` directly with `file://` won't work because of browser security restrictions on scripts). The easiest options:

```bash
# Python 3
python3 -m http.server 8000

# or Node.js
npx serve .
```

Then visit `http://localhost:8000` (or whatever port your tool prints).

## How to play

- **Player 1:** `WASD` to move, `SPACE` to kick
- **Player 2 (local multiplayer):** Arrow keys to move, `ENTER` to kick
- Stand near the ball to control it — hold it for 2 seconds to charge a **power shot**
- First to **3 goals** (or whoever's ahead when the 2-minute clock runs out) wins

### Modes

| Mode | Description |
|---|---|
| 🤖 VS Bot | Play solo against an AI opponent |
| 👥 Local 2 Player | Two players, one keyboard |
| 🌐 Host Online Match | Creates a room code your friend can use to join from anywhere |
| 🔗 Join Online Match | Enter a friend's room code to connect |

Online matches connect two browsers directly (peer-to-peer via [PeerJS](https://peerjs.com/)) — no backend server needed.

## Deploying to GitHub Pages

1. Push this repo to GitHub.
2. In your repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to `Deploy from a branch`, pick your default branch (e.g. `main`) and the `/ (root)` folder.
4. Save — GitHub will give you a URL like `https://<your-username>.github.io/<repo-name>/`.

## Project structure

```
.
├── index.html   # loads Phaser + PeerJS from CDN, then game.js
├── game.js      # all game logic (scenes, physics, UI, online multiplayer)
└── README.md
```

## Built with

- [Phaser 3](https://phaser.io/) — HTML5 game framework (loaded via CDN)
- [PeerJS](https://peerjs.com/) — WebRTC peer-to-peer connections (loaded via CDN)

## License

MIT — do whatever you'd like with it.
