1. Use a public server/VPS that is reachable by your intended users.
2. Set a strong JWT_SECRET.
3. Put HTTPS in front of Node.js.
4. Keep data/ and uploads/ on persistent storage.
5. Back up messages and uploads.
6. If exposing the server directly, allow only the required ports.
7. For larger deployments, move users/messages to a real database and uploads to object storage.
8. For reliable WebRTC across restrictive NATs, configure a TURN server.
