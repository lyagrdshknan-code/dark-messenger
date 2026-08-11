# Dark Messenger Online v4

A real-time dark messenger. Features: accounts, hashed passwords, avatars, online presence, persistent `data/messages.json`, file/image/voice messages, emoji, reply/edit/delete, search, admin clear, multiple voice rooms, WebRTC voice, screen sharing and responsive dark UI.

## Local
Install Node.js 18+. In this folder run `npm install` then `npm start`. Open `http://localhost:3000`.

The server binds to `0.0.0.0`, so on the same LAN you can use `http://YOUR-PC-IP:3000` after allowing Node through Windows Firewall.

## Public Internet
A PC on localhost is not automatically public. For a real public site, deploy this folder to a Node.js host. Set start command `npm start` and environment variable `JWT_SECRET` to a long random value. Use HTTPS in production because microphone, screen sharing and browser notifications require a secure origin outside localhost.

Chat history is stored in `data/messages.json` and uploads in `uploads/`. A host with an ephemeral filesystem can erase these on restart, so production needs persistent disk or database/object storage.

WebRTC includes public STUN servers. For networks with strict NAT, a TURN server may be required.
