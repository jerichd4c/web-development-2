<a id="readme-top"></a>

<br />
<div align="center">
  <img src="https://img.shields.io/badge/Web%20Development%202-URU-blue?style=for-the-badge" alt="Web Development 2" width="320" height="40">

<h3 align="center">Web Development 2 - Sebastian Cohen</h3>

  <p align="center">
    Repository for the Web Development 2 course at URU. It gathers the final versions of the class projects — real-time apps built with WebRTC and Socket.IO.
  </p>
</div>

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-repository">About The Repository</a>
      <ul>
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
    <li><a href="#repository-structure">Repository Structure</a></li>
    <li><a href="#main-projects">Main Projects</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
  </ol>
</details>

## About The Repository

This repository brings together the material covered in the **Web Development 2** course at URU. Its purpose is to keep the final, working version of each project in one organized place — real-time, peer-to-peer web applications built around WebRTC and Socket.IO.

Each project folder is self-contained and has its own README with setup instructions and implementation details.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Built With

* [![Node.js][Node-badge]][Node-url]
* [![Express][Express-badge]][Express-url]
* [![Socket.IO][SocketIO-badge]][SocketIO-url]
* WebRTC (native browser API)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Getting Started

Each project has its own dependencies and run instructions — see its individual README linked in [Main Projects](#main-projects).

### Prerequisites

* Node.js and npm

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/jerichd4c/web-development-2.git
   ```
2. Open the folder for the project you want to run.
3. Follow that project's own README.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Repository Structure

These are the projects currently available in the repository:

* `webrtc-video-chat/`: peer-to-peer video calling app with a host-gated waiting room, moderation controls, screen sharing, and a shared whiteboard overlay.
* `realtime-collaborative-whiteboard/`: a real-time collaborative whiteboard with drawing tools and live voice chat.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Main Projects

### [WebRTC Video Chat](webrtc-video-chat/README.md)
A peer-to-peer video calling app with a host/guest waiting room and moderation controls.
* **Features**: host-gated room access, mute/kick moderation, screen sharing, text chat, a shared whiteboard overlay.
* **Documentation**: [Project README](webrtc-video-chat/README.md)

### [Realtime Collaborative Whiteboard](realtime-collaborative-whiteboard/README.md)
A browser-based whiteboard where every stroke and shape syncs instantly across everyone in the room, with live voice chat.
* **Features**: drawing tools, shapes, real-time sync over Socket.IO, peer-to-peer voice chat via WebRTC.
* **Documentation**: [Project README](realtime-collaborative-whiteboard/README.md)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Roadmap

This roadmap summarizes the course progress and can keep growing as new units or assignments are added.

- [x] Peer-to-peer video calling with WebRTC signaling over Socket.IO.
- [x] Real-time collaborative drawing synced over Socket.IO, with WebRTC voice chat.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

[Node-badge]: https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white
[Node-url]: https://nodejs.org/
[Express-badge]: https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white
[Express-url]: https://expressjs.com/
[SocketIO-badge]: https://img.shields.io/badge/Socket.IO-010101?style=for-the-badge&logo=socketdotio&logoColor=white
[SocketIO-url]: https://socket.io/
