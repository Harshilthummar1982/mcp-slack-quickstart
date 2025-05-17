# MCP Server Quickstart with Slack Integration

**Setup a Model Context Protocol (MCP) server with Slack notifications in 60 seconds.**

---

## 🚀 Usage

### 1. Ensure you have [Bun](https://bun.sh) installed.

### 2. Clone the repo and install dependencies:

```bash
git clone https://github.com/Harshilthummar1982/mcp-slack-quickstart mcp-slack-quickstart && cd mcp-slack-quickstart && bun install
```

### 3. Install the `node-fetch` dependency:

```bash
bun add node-fetch
```

### 4. Set your Slack webhook URL in the `server.ts` file:

```ts
// Replace with your actual Slack webhook URL
const SLACK_WEBHOOK_URL = "YOUR_SLACK_WEBHOOK_URL";
```

### 5. Copy the absolute path to the server file:

```bash
realpath server.ts | pbcopy
```

### 6. Open the Claude desktop app config:

```bash
vim ~/Library/Application\ Support/Claude/claude_desktop_config.json
```

### 7. Add the server config with the path from step 5:

```json
{
  "mcpServers": {
    "weather-quickstart": {
      "command": "bun",
      "args": ["/absolute/path/to/mcp-quickstart/server.ts"]
    }
  }
}
```

### 8. Restart the Claude desktop app and ask for the weather!

---

## 📩 Slack Integration

This server sends notifications to Slack whenever:

* ✅ The server starts up
* 🛠 A tool list is requested
* 🌦 A weather query is made (including the location)
* ❓ An unknown tool is requested
* ❌ Any error occurs

All interactions with the Claude Desktop tool will be logged to your specified Slack channel, providing **real-time visibility** into tool usage.

---

## 📎 Related

* [Bun Documentation](https://bun.sh/docs)
* [Slack Incoming Webhooks](https://api.slack.com/messaging/webhooks)

---

Let me know if you'd like it converted into a `.md` file or hosted in your repo!
