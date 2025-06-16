# streamin
Lightweight stream from any device to another device using same WiFi

# 📡 Local RTMP Server with OBS on macOS

This project sets up a **local RTMP server** using **Docker** and **NGINX with the RTMP module**. You can stream your macOS screen (including system audio) using **OBS Studio** to this local server, which can be played on any device (e.g., Android TV) connected to the same Wi-Fi network.

---

## 🧰 Requirements

- [Docker](https://www.docker.com/products/docker-desktop)
- [OBS Studio](https://obsproject.com/)
- [BlackHole 2ch](https://existential.audio/blackhole/) (for system audio capture)

---

## 🛠️ Setup Instructions

### 1. Clone the Repo
### 2. Run start the dockerfile to build and run
To build:
```bash
docker build -t local-rtmp .
```
To run:
```bash
docker run -d -p 1935:1935 -p 8080:8080 --name local-rtmp-server local-rtmp
```
### 2. Stream capture from OBS
Use custom as service is Stream settings.
```bash
Server: rtmp://<ip-address>:1935/live
Stream Key: stream
```

### 3. Use VLC
Use VLC or any other media player to connect to the stream.

Really very little use this repo, unless you really need it.
