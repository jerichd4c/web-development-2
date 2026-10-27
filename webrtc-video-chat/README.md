<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a id="readme-top"></a>

<!-- PROJECT LOGO -->
<div align="center">
  <a href="https://github.com/jerichd4c/web-development-2/tree/main/webrtc-video-chat">
    <img src="https://raw.githubusercontent.com/jerichd4c/logos/main/javascript_logo.svg" alt="Logo" width="80" height="80">
  </a>
</div>

<div align="center">

<h3 align="center">WebRTC Video Chat</h3>

  <p align="center">
    A real-time video calling app with a host/guest waiting room, moderation controls, text chat, screen sharing, and a shared whiteboard.
    <br />
    <a href="https://webrtc-video-chat-3uci.onrender.com"><strong>Try the live demo »</strong></a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#features">Features</a></li>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#known-limitations">Known Limitations</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

A peer-to-peer video calling app built on top of WebRTC, with a small Socket.IO server acting purely as a **signaling server** (SDP offers/answers and ICE candidates only — no video/audio ever passes through it). The first person to join a room becomes its **host**, who approves or rejects everyone else trying to join and can moderate the call once it's running.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Features

* **Host-gated waiting room:** the first user in a room becomes host; anyone joining afterward waits until the host accepts or rejects them.
* **Moderation (host only):** mute a specific guest, mute everyone at once, request a guest to unmute, and kick a user from the call.
* **Camera & mic controls:** toggle your own camera/mic, and raise your hand to signal the room.
* **Screen sharing** via `getDisplayMedia`.
* **Text chat**, broadcast to everyone currently in the room.
* **Shared whiteboard overlay:** a lightweight synced canvas (color picker, brush size, clear) that any participant can open mid-call.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Built With

* [![Node.js][Node-badge]][Node-url]
* [![Express][Express-badge]][Express-url]
* [![Socket.IO][SocketIO-badge]][SocketIO-url]
* WebRTC (native browser API, for peer-to-peer video/audio and screen share)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

### Prerequisites

* Node.js and npm

### Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/jerichd4c/web-development-2.git
   ```
2. Navigate to the project directory:
   ```sh
   cd web-development-2/webrtc-video-chat
   ```
3. Install dependencies:
   ```sh
   npm install
   ```
4. Start the server:
   ```sh
   npm start
   ```
5. Open `http://localhost:3000` in a browser tab — that first tab becomes the host. Open it in more tabs/devices to join as a guest.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Usage

The first participant to open the app becomes the room's host and gets in immediately. Everyone after that sees a waiting screen until the host accepts them from the notifications panel. Once in the call, use the control bar to mute/unmute, toggle your camera, raise your hand, share your screen, or open the shared whiteboard — text chat and (for the host) moderation actions like **Mute All** or kicking a guest are available throughout the call.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- KNOWN LIMITATIONS -->
## Known Limitations

* **Single shared room:** the room id is currently hardcoded, so everyone who opens the app lands in the same call — there's no support yet for creating or joining separate rooms.
* **Host has no failover:** if the host disconnects, their admin privileges are simply freed up — there's no mechanism to reassign the host role to a remaining guest, and no persistence of the call once everyone leaves.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
[Node-badge]: https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white
[Node-url]: https://nodejs.org/
[Express-badge]: https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white
[Express-url]: https://expressjs.com/
[SocketIO-badge]: https://img.shields.io/badge/Socket.IO-010101?style=for-the-badge&logo=socketdotio&logoColor=white
[SocketIO-url]: https://socket.io/
