<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a id="readme-top"></a>

<!-- PROJECT LOGO -->
<div align="center">
  <a href="https://github.com/jerichd4c/web-development-2/tree/main/realtime-collaborative-whiteboard">
    <img src="https://raw.githubusercontent.com/jerichd4c/logos/main/javascript_logo.svg" alt="Logo" width="80" height="80">
  </a>
</div>

<div align="center">

<h3 align="center">Realtime Collaborative Whiteboard</h3>

  <p align="center">
    A real-time collaborative digital whiteboard — drawing tools, shapes, and live voice chat, synced instantly across everyone in the room.
    <br />
    <a href="https://realtime-collaborative-whiteboard-wvsa.onrender.com"><strong>Try the live demo »</strong></a>
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

A browser-based whiteboard, inspired by [Excalidraw](https://excalidraw.com/), where every stroke, shape, and cursor action is broadcast in real time to everyone connected via Socket.IO. On top of drawing, peers can also talk to each other over a live voice channel established with WebRTC — no separate call app needed.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Features

* **Drawing tools:** select/move, pan, pencil, eraser, line, rectangle, circle/ellipse, triangle, text, and image insertion.
* **Customizable stroke:** color picker and adjustable stroke size.
* **Real-time sync:** every draw and move action is broadcast instantly to the rest of the room over Socket.IO.
* **Voice chat:** peer-to-peer audio via WebRTC, with per-user mute and speaker controls and a live connected-users panel.
* **Light / dark theme**, persisted locally.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Built With

* [![Node.js][Node-badge]][Node-url]
* [![Express][Express-badge]][Express-url]
* [![Socket.IO][SocketIO-badge]][SocketIO-url]
* WebRTC (native browser API, for peer-to-peer audio)

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
   cd web-development-2/realtime-collaborative-whiteboard
   ```
3. Install dependencies:
   ```sh
   npm install
   ```
4. Start the server:
   ```sh
   npm start
   ```
5. Open `http://localhost:3000` in two or more browser tabs/devices to collaborate.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Usage

Everyone who opens the app joins the same shared whiteboard room automatically. Pick a tool from the floating top toolbar to draw shapes, freehand strokes, or text; use **Select** to move existing objects and **Pan** to move around the canvas. Grant microphone access to talk with everyone else currently connected — use the mic button in the **Users** panel to mute/unmute yourself, and the speaker button on any peer to mute them locally.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- KNOWN LIMITATIONS -->
## Known Limitations

* **Single shared room:** the room id is currently hardcoded, so all visitors land in the same whiteboard — there's no support for separate/private rooms yet.
* **No persistence:** the canvas only lives in each connected browser's memory. Nothing is saved server-side, and a user who joins after drawing has started will only see *new* strokes from that point on, not the existing scene.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
[Node-badge]: https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white
[Node-url]: https://nodejs.org/
[Express-badge]: https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white
[Express-url]: https://expressjs.com/
[SocketIO-badge]: https://img.shields.io/badge/Socket.IO-010101?style=for-the-badge&logo=socketdotio&logoColor=white
[SocketIO-url]: https://socket.io/
