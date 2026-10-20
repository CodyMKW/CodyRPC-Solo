# 🎮 CodyRPC-Solo

A personal, serverless Discord Rich Presence gateway built specifically for **Cody**. It continuously syncs Nintendo Switch activity directly to Discord using Cloudflare Workers—no desktop app or extra background processes required.

## 📌 Personal Notes & Specs

- **Worker Domain:** `https://codyrpc-solo.codymkw.workers.dev`
- **Discord App Client ID:** `1543356402179899432`
- **Primary Auth:** Secured via `CODYRPC_TOKEN` secret set in Cloudflare Worker environment variables.

## ⚡ How It Runs

1. **Fetch:** Cloudflare Worker cron triggers poll the `nxapi` presence service using my **Nintendo Account (NSA) ID**.
2. **Transform:** Process settings (clean game names, play time display, custom status text/buttons, manual override).
3. **Push:** Sends updated activity payloads directly to Discord via OAuth2 (`sdk.social_layer_presence`).

## ⚙️ Core Configuration Options

- **Home Menu Display:** Toggle "On the Home Menu" status when no game is active.
- **Game Name Cleanup:** Automatically strips suffix clutter like "for Nintendo Switch".
- **Play Time & Friend Code:** Show total gameplay hours or display Switch Friend Code on profile hover.
- **Custom Buttons / Status:** Direct links to Twitch/website or custom text status overrides.
- **Manual Mode:** Force custom activity name, details, and state when needed.

## 🔗 Quick Reference Links

- **Presence Auth Server:** [nxapi-auth.fancy.org.uk](https://nxapi-auth.fancy.org.uk)
- **Default Switch Logo Asset:** `https://codymkw.github.io/switch/nintendo_switch_logo.png`

---
*CodyRPC-Solo · Personal utility project*