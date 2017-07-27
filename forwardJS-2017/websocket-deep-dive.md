## A Full Stack Websocket Deep Dive

`var websocket = new Websocket('ws://localhost:8080');`

- ws vs wss
  - use wss in real world situations (s for secure)

- `websocket.onerror` and `websocket.onclose` come as a pair.

## Why Websockets?
- Websockets are a two way communication
- Websockets have better performance than AJAX requests

## Best time to use Websockets?
- Games
- Chat
- Background notifications
- Streaming data

## Debug Tools
- Chrome Dev Tools > Websocket tab

## What can you send over Websockets?
> Basically anything! You can send images, sounds, files, whatever!

## TCP vs UDP
> TCP and UDP are the most common communication protocols

- TCP
  - Websocket uses TCP. Makes sure all web packets get delivered
  - TCP makes sure ALL packets get delivered
- UDP
  - UDP sends packets very fast, but can drop a packet
  - UDP is good for streaming video, doesn't matter if you drop a packet.

## Libraries and Subprotocols
- Common Libraries
  - WAMP
  - Socket.io
    - One of the best libaries for websockets in JS
    - Defaults to long polling if no support for websockets

- Protocol example
`ws.onopen = function () {
  if (ws.protocol = 'chatMessage') {
    ...
  } else {
    ...
  }
}`

## Do you need your own server?
- You can run websockets without a server, especially for mini personal projects

## See what websockets are open on your computer
- Type the following into your terminal
`lsof -Pn -i4`

## Advice
- Always use wss://
- Always use port 443
- Increase file descriptor count
- Look at available sub protocols and libraries
- Use Node.js
