# Space Hex Tactics

Impulse-based, Newtonian hex space combat between the Dogahr and the Martians.

**Play:** https://pinecone0333.github.io/Space-Hex-Battles/

## Online two-player
1. One player clicks **Host an online game** and sends the 5-letter code to the other.
2. The other player types the code and clicks **Join**.
3. Each player builds their own fleet; the host presses **Launch battle**.
4. Every impulse, both players give orders and press **Continue** (Enter). The impulse resolves when both are ready.

The two browsers connect directly (WebRTC via PeerJS). The host's browser runs the battle; the joining player's browser shows it and sends orders. Most home networks work; some strict school or office networks block direct connections.
