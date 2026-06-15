
## What is this project?

NodeRed_Dashboard is a Docker-based project that connects a Minecraft Java server, Discord, and Node-RED. It provides a web dashboard to monitor chat, send messages, and control basic Minecraft server functions from a single interface.

## How is this project installed?

### Requirements

- Docker Desktop

### Setup

1. Clone the repository:

```bash
git clone https://github.com/ordjo794/NodeRed_Dashboard.git
cd NodeRed_Dashboard
```

2. Create a `.env` file next to `compose.yml`:

```env
RCON_PASSWORD=your_minecraft_rcon_password
DISCORD_TOKEN=your_discord_bot_token
DISCORD_WEBHOOK=your_discord_webhook_url
```

3. Start the project:

```bash
docker compose up -d
```

### Access

- **Minecraft Server:** `localhost:25565`
- **Node-RED Editor:** `http://localhost:1880`

If the Node-RED flows are not loaded automatically, import `flows.json` through **Menu → Import** and click **Deploy**.

## How does it work?

The project uses Docker Compose to run a Minecraft Java server, Node-RED, and an MQTT broker.

- Messages sent from the Node-RED dashboard are forwarded to Discord using a webhook.
- Messages received from Discord are displayed on the dashboard and sent to the Minecraft in-game chat.
- The dashboard can control the Minecraft server's weather and time through RCON using `@tomsith/node-red-contrib-minecraft`.

## Security

Keep your `.env` file private and never commit it to the repository.
