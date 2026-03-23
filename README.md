# BASIS Tools

On-chain analytics and interactive tools for the **$BASIS** token on Solana.

Built with vanilla HTML/CSS/JS — no frameworks, no build step. Just open and run.

---

## Tools

### Terminal

A retro hacker-style command line interface for querying live on-chain $BASIS data.

**Features:**
- 16 commands — `holders`, `whales`, `balance`, `supply`, `tx`, `info`, `rank`, `compare`, `chart`, `watch`, `export`, `alias`, `motd`, `theme`, `matrix`, `moon`
- Matrix rain background with theme-matched colors
- Tab autocomplete, persistent command history, pipe filtering (`whales | top 5`)
- Custom aliases (`alias w = whales`)
- Clickable wallet addresses — click any address to check its balance
- Copy buttons on output blocks
- Multiple terminal tabs
- 4 color themes — Green, Amber, Cyan, Red
- Sound effects (toggleable) — keypress clicks, command beeps, error buzz
- Boot sequence animation with system check lines
- Glitch effect on errors
- `watch` command for auto-refreshing data every 30s
- `export` command to download output as .txt
- Easter eggs — `matrix` (fullscreen rain), `moon` (ASCII rocket)
- Status bar with connection status, last command, holder count, live clock

### Holder Map

An interactive visualization of all $BASIS token holders as floating squares.

**Features:**
- Spiral-packed squares — each wallet is a perfect square, sized by holdings
- Zoom in/out (scroll, pinch, buttons) up to 80x — deep into dust-level wallets
- Pan by dragging the background
- Drag individual wallets with physics repulsion — nearby wallets gently push away
- Dynamic zoom labels — numbers appear and scale as you zoom into smaller holders
- Bonding curve detection — top holder flagged as Pump.fun Bonding Curve with pulse glow
- Top 10 rank badges inside wallet squares
- Click any wallet to lock info panel with full details
- OrbMarkets integration — each wallet links to `orbmarkets.io/address/{wallet}`
- Search wallets — type to highlight and zoom to matching addresses
- Tier system — Whale, Shark, Dolphin, Fish, Shrimp, Plankton, Dust
- Tier legend with holder counts, click to filter, double-click to zoom to tier
- 300 animated particles with connection lines between nearby particles
- Proximity lines between same-tier neighbors
- Hover ripple effects
- Smooth animated zoom transitions
- Stats bar — total held, average, median
- Pixel grid background with parallax
- Export current view as PNG

---

## Data Source

All data is fetched live from **Solana Mainnet** via the [Helius RPC](https://helius.dev/) API.

- Token accounts — `getTokenAccounts` (DAS API)
- Token metadata — `getAsset` (DAS API)
- Transaction history — Helius parsed transactions REST API

No backend. No database. Everything is client-side and reads directly from the blockchain.

---

## Token

| | |
|---|---|
| **Name** | BASIS |
| **Symbol** | $BASIS |
| **Chain** | Solana |
| **Mint** | `A5BJBQUTR5sTzkM89hRDuApWyvgjdXpR7B7rW1r9pump` |
| **Supply** | 1,000,000,000 |
| **Decimals** | 6 |

---

## Setup

No dependencies. No build tools. Just static HTML files.

**Run locally:**
```
git clone https://github.com/YOUR_USERNAME/basis-tools.git
cd basis-tools
open terminal/index.html
```

**Deploy to GitHub Pages:**
1. Push to GitHub
2. Go to **Settings → Pages**
3. Source: **Deploy from a branch**
4. Branch: `main`, folder: `/ (root)`
5. Your tools will be live at `https://YOUR_USERNAME.github.io/basis-tools/`

---

## Project Structure

```
basis-tools/
├── README.md
├── terminal/
│   └── index.html        # BASIS Terminal
├── holder-map/
│   └── index.html        # Holder Map Visualization
└── genesis/
    └── index.html         # Genesis NFT Collection Page
```

---

## Design System

All tools share a consistent visual language:

- **Font** — IBM Plex Mono
- **Color** — `#78b15a` green on black
- **Panel** — Rounded corners (14px), scanline overlay, inset shadow, green glow
- **Module bar** — Dots + label + status with green gradient
- **Controls** — Dashed borders, green accents, uppercase labels
- **Separators** — Dashed line with centered label

---

## Tech Stack

- HTML5 Canvas (Holder Map rendering, Matrix rain)
- Web Audio API (Terminal sound effects)
- Helius RPC / DAS API (on-chain data)
- localStorage (command history, aliases, theme preference)
- Zero dependencies — no npm, no React, no build step

---

## Links

- **OrbMarkets** — [orbmarkets.io](https://orbmarkets.io/)
- **NFT Builder** — [nft.databasis.info](https://nft.databasis.info/)
- **Genesis Collection** — [Magic Eden](https://magiceden.io/marketplace/basis) · [Tensor](https://www.tensor.trade/trade/basis)

---

## License

MIT
