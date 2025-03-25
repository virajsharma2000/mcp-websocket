# MCP WebSocket Server

This project implements an MCP (Model Context Protocol) server with WebSocket enhancements for real-time data updates. It allows clients to make standard MCP requests while also enabling WebSocket-based subscriptions to receive push notifications when new data becomes available.

## Features
- **MCP Server (Port 8080):** Handles standard MCP requests from clients.
- **WebSocket Server (Port 8765):** Allows clients to subscribe for real-time updates.
- **Push Notifications:** Sends updates to all subscribed clients when new data is available.
- **Async Architecture:** Uses `asyncio` for efficient non-blocking operations.

## Installation
1. Clone this repository:
   ```sh
   git clone https://github.com/your-repo/mcp-websocket-server.git
   cd mcp-websocket-server
   ```
2. Install dependencies:
   ```sh
   pip install websockets mcp-sdk  # Replace with actual MCP SDK package name
   ```

## Usage
### Start the Server
Run the following command to start both the MCP and WebSocket servers:
```sh
python server.py
```

### Connecting via WebSockets
Clients can connect to the WebSocket server (`ws://localhost:8765`) and subscribe to updates by sending:
```json
{"action": "subscribe"}
```

### Sending MCP Requests
MCP clients can send requests to the MCP server at `http://localhost:8080` with a payload like:
```json
{"method": "get_data"}
```
The server will respond with:
```json
{"result": "Here is your data!"}
```

## License
This project is licensed under the MIT License.

## Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss what you’d like to change.

## Contact
For questions or suggestions, reach out via [virajsharma@sharmaviraj.com].

# mcp-websocket
This server implements an MCP (Model Context Protocol) server with WebSocket enhancements for real-time data updates.
