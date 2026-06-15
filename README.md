# NodeRed_Dashboard
Dashboard for a Minecraft server
# NodeRed_Dashboard

A Docker Compose project that runs a Minecraft Java server alongside a Node-RED instance. Secrets such as passwords and Discord credentials are stored in a local `.env` file instead of the repository.

## Requirements

- Docker Desktop (or Docker Engine with Docker Compose)

## Setup

Create a `.env` file in the project root (next to `compose.yml`) and add your credentials:

```env
RCON_PASSWORD=your_secure_password
DISCORD_TOKEN=your_discord_bot_token
DISCORD_WEBHOOK=your_discord_webhook_url
```

## Run

Start the project:

```bash
docker compose up -d
```

Stop the project:

```bash
docker compose down
```

## Access

| Service | Address |
|---------|---------|
| Minecraft Server | `localhost:25565` |
| Node-RED Editor | `http://localhost:1880` |

## Importing Flows

If the flows are not loaded automatically:

1. Open `http://localhost:1880`
2. Go to **Menu → Import**
3. Select `flows.json`
4. Click **Import**
5. Click **Deploy**

## Security

Keep your `.env` file private and never commit it to the repository.
