# AXL SESSION MANAGER — Session Management Platform

Premium Telegram session management bot (Pyrogram + Telethon) with bulk operations, email binding, proxy pools, and access control.

## Access: Force-Join

The bot is **public**, but users must **join your channel/group** before they can use it. Membership is verified automatically.

| Env var | Description |
|---------|-------------|
| `FORCE_JOIN_CHAT` | `@username`, `https://t.me/username`, or numeric chat id (`-100...`) |
| `FORCE_JOIN_ENABLED` | `true` / `false` (default: auto-on when a target is set) |
| `CHANNEL_LINK` | Join button URL; public username used as fallback target |
| `ADMIN_IDS` | Real **owner** Telegram user IDs (comma-separated) |

**Important:** Add the bot as an **admin** in that channel/group so it can verify membership.

### Owner admin protection

- `ADMIN_IDS` in `.env` / Railway = **real owners** (`OWNER_ADMIN_IDS`).
- Admins added through the bot panel **cannot**:
  - Remove owner admins
  - Ban owner admins
  - Add or remove other admins (only owners can)
- Owner admins can only be changed by editing `ADMIN_IDS` in environment variables.

## Setup

1. Copy `.env.example` → `.env` and fill in:
   - `API_ID` / `API_HASH` (from https://my.telegram.org)
   - `BOT_TOKEN` (from @BotFather)
   - `ADMIN_IDS` (your Telegram user ID, comma-separated)
   - `FORCE_JOIN_CHAT` / `CHANNEL_LINK` (optional force-join)
2. `pip install -r requirements.txt`
3. `python main.py` (or `./start.sh`)

## Main Features

- Upload & manage packs of Telethon / Pyrogram `.session` files
- Bulk verify, spam scan, age check, mail check
- Free Temp-Mail + Self-Mail Vault (Gmail permutation) email binding
- Profile edit (name, bio, username, avatar)
- 2FA management, device control, clean chats/contacts
- Community actions (join/leave, broadcast, react, views, report, scrape)
- Proxy pool with FloodWait failover
- Format conversion, export strings/hex, split by country/spam
- Full admin panel

## Requirements

See `requirements.txt`.
