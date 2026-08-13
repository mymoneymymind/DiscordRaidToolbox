# DISCORD RAID TOOLBOX

A Discord raid bot built on **discord.js v13**.
Credits to [t.me/yackinnn](t.me/yackinnn)

> **Authorized lab use only.** This tool is meant to stress-test a Discord
> moderation / anti-raid bot you own, against a throwaway test guild you control.
> Do not point it at servers you do not own or have permission to test against.

## Credit

Created by **yackinnn** — https://t.me/yackinnn

## Requirements

- [Node.js](https://nodejs.org/) (v24 used in testing; v13-compatible)
- A Discord bot token (from the [Developer Portal](https://discord.com/developers/applications))
- **Privileged Gateway Intents enabled** for the bot:
  - `MESSAGE CONTENT`
  - `SERVER MEMBERS`

  Without these, `message.content` is empty and no command will run.

## Setup

1. Install dependencies:
   ```sh
   npm install
   ```
2. Open `settings.json` and fill in your values (token, prefix, server
   name, channel name, etc.).
3. Run the bot:
   ```sh
   node index.js
   ```

## Configuration (`settings.json`)

| Key | Description |
|-----|-------------|
| `token` | Your bot token |
| `prefix` | Command prefix (default `.`) |
| `nameserver` | Name applied to the target server |
| `channelname` | Name for created channels |
| `image` | Raid image URL |
| `numberchannelmax` | Max channels to create |
| `numbermessagemax` | Max messages per channel |
| `noRaidServerID` | Server ID where commands are blocked |
| `logschannelid` | Channel ID for command logs |
| `creditname` | Bot owner name shown in output |
| `helpRAIDcommand` | Command name that lists raid commands |

## Commands (prefix `.`)

| Command | Effect |
|---------|--------|
| `.des` | Destroy the server |
| `.del` | Delete all channels |
| `.red` | Wipe using a custom invite link + channel name |
| `.r` | Grant self admin role (bot must have perms) |
| `.exit` | Make the bot leave the server |
| `.help` | Show anti-raid–style help |
| `.help1212` | Send raid commands to your DMs |
| `.gay` | Create many purple "gay" roles and assign to everyone |
| `.ban` | Ban all members |
| `.list` | List servers with their IDs |
| `.xinvite` | Get an invite for a server ID |
| `.invite` | Invite the bot |

## Notes

- The bot only requires `discord.js` and the native `https` module.
- `install.bat` runs `npm install`. Do **not** install the legacy
  `discord.js-v11-stable` branch — it breaks this v13 code.
- Intents were fixed to include `MESSAGE_CONTENT` + `GUILD_MEMBERS` so
  command parsing works against current Discord gateways.
