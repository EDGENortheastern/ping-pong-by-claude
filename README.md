# Ping Pong (by Claude)

A browser-based ping pong game generated entirely by Claude, Anthropic's AI assistant. The game runs in a single HTML file with no dependencies or build step. It uses the Claude API to generate new visual themes on demand.

Live: [https://edgenortheastern.github.io/ping-pong-by-claude](https://edgenortheastern.github.io/ping-pong-by-claude)
## About

This project was created through a conversation with Northeastern's Claude, [claude.ai](https://claude.northeastern.edu/). The user described the desired output — a playable pong game with a retro aesthetic and AI-powered theming, and Claude authored all of the code: the game loop, canvas rendering, collision physics, scorekeeping, and Anthropic API integration. No code was written by hand.

---

## Requirements

- A modern web browser (Chrome, Firefox, Safari, or Edge)
- An internet connection (required for Claude-generated themes and Google Fonts)

---

## Installation

```bash
git clone https://github.com/your-username/ping-pong.git
cd ping-pong
open index.html
```

No package manager, build tool, or local server is required. Open `index.html` directly in a browser.

---

## Usage

### Controls

| Input | Action |
|-------|--------|
| `↑` or `W` | Move left paddle up |
| `↓` or `S` | Move left paddle down |
| Play button | Start or pause the game |
| Claude Style button | Request a new colour theme from Claude |
| Reset button | Clear scores and return the ball to the centre |

The right paddle is controlled by the computer. The left paddle is controlled by the user.

### Scoring

A point is awarded each time the ball passes the opponent's paddle and exits the left or right edge of the court. The score is displayed above the game canvas and updates immediately after each point.

---

## How Claude theming works

Pressing the **✦ Claude Style** button sends a request to the Claude API (`claude-sonnet-4-20250514`) asking it to generate a colour theme as a JSON object. The response includes hex and rgba values for the background, court, net, paddles, ball, ball trail, and accent colour, along with a short theme name. The game parses the response and applies the new colours to the canvas immediately without reloading the page.

Example themes Claude may generate: Neon Noir, Deep Ocean, Lava Cave, Arctic Console.

---

## File structure
