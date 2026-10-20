# AccStore — Session Management Platform

Premium Telegram session management bot (Pyrogram + Telethon) with bulk operations, email binding, proxy pools, and access control.

## New Feature: Access Control

The bot is **private by default**. Only users listed in `ADMIN_IDS` (from `.env`) and users granted access by an admin can use it.

### Commands (Admin / Owner only)

| Command | Description |
|---------|-------------|
| `/adduser <user_id>` | Grant a user access to the bot |
| `/removeuser <user_id>` | Revoke a user's access |
| `/userlist` | Show all admins + users who currently have access |

Access list is persisted in the bot's meta storage and survives restarts.

## Setup

1. Copy `.env.example` → `.env` and fill in:
   - `API_ID` / `API_HASH` (from https://my.telegram.org)
   - `BOT_TOKEN` (from @BotFather)
   - `ADMIN_IDS` (your Telegram user ID, comma-separated)
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
