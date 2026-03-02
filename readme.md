
# Media Server

A simple Docker-based media server using the following stack:
## Stack Overview

This setup includes:

###  Jellyfin (Media Player)
- Web UI: http://localhost:8096  
- Streams your movies and TV shows
- Reads media files from `/data`

###  Sonarr (TV Automation)
- Web UI: http://localhost:8989  
- Automatically downloads and manages TV shows

### Radarr (Movie Automation)
- Web UI: http://localhost:7878  
- Automatically downloads and manages movies

### Prowlarr (Indexer Manager)
- Web UI: http://localhost:9696  
- Manages torrent indexers and connects them to Sonarr & Radarr

### qBittorrent (Downloader)
- Web UI: http://localhost:8080  
- Handles torrent downloads
- Uses `/data` for completed downloads

### FlareSolverr
- Runs on port 8191  
- Bypasses Cloudflare protection for supported indexers


## Setup

1. Install Docker and Docker Compose.
2. Navigate to the project directory:
   ```bash
   cd ~/MediaServe```
3. Start the services:
   ```bash
    docker compose -f mediaserver.yaml up --build``
4. Open jellyfin browser
   ```bash 
      http://localhost:8080
    ```

