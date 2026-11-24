# Space Hex Tactics

Impulse-based, Newtonian hex space combat between the Dogahr and the Martians.

**Play:** https://pinecone0333.github.io/Space-Hex-Battles/

## Online two-player
1. One player clicks **Host an online game** and sends the 5-letter code to the other.
2. The other player types the code and clicks **Join**.
3. Each player builds their own fleet; the host presses **Launch battle**.
4. Every impulse, both players give orders and press **Continue** (Enter). The impulse resolves when both are ready.

The two browsers connect directly (WebRTC via PeerJS). The host's browser runs the battle; the joining player's browser shows it and sends orders. Most home networks work; some strict school or office networks block direct connections.

## Source backup
`index.html` is the built game. The real source lives in `src/` and is updated with every change:

- `src/impulse.js` (game and AI), `src/mp.js` (online play), `src/body.html`, `src/style.css`, music and sound files, `src/rules.md` (the full design log).
- To rebuild: `cd src && python3 build.py`, which writes `index.html` (GitHub version, with online play) and `index_artifact.html` (no networking).
- `tools/shipstats` and `tools/weapchart` build the ship stats page and the weapons chart. They read the built game with Playwright and Chrome; their paths assume the files are in `/home/claude/...`, so adjust them before running elsewhere.
- `tools/mpserver` is the local PeerJS server used only for testing online play.
