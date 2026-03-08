# 🎬 plex-arr-stack - Easy Media Server Setup

[![Download plex-arr-stack](https://img.shields.io/badge/Download-plex--arr--stack-4c1?style=for-the-badge&logo=github&color=blue)](https://github.com/aliadel009/plex-arr-stack/releases)

---

## 📦 What is plex-arr-stack?

plex-arr-stack is a ready-to-use bundle of popular media server tools. It uses Docker Compose to set up Plex, Sonarr, Radarr, Lidarr, Prowlarr, qBittorrent, and some extras together. This stack lets you manage, download, and stream your music and movies with one simple command. 

You do not need to install each program separately or deal with complicated configurations. The stack works on Windows, using Docker as its base, and handles everything in the background. Once set up, you can access all tools from your web browser.

---

## 🖥 System Requirements

Before installing, check these minimum needs for your Windows PC:

- **Operating System:** Windows 10 (64-bit) or later
- **CPU:** 4-core processor or better
- **Memory:** At least 8 GB of RAM
- **Storage:** Minimum 100 GB free space, depending on your media files
- **Internet:** Stable connection to download containers and media
- **Docker:** Must be installed and running (Windows version with WSL2 backend preferred)

---

## ⚙️ Getting Ready

You will need Docker on your Windows machine. Docker creates containers that run the apps safely and efficiently. Follow these simple steps to get Docker ready:

1. Visit the [Docker official website](https://docs.docker.com/docker-for-windows/install/) to download Docker Desktop for Windows.
2. Run the installer and follow instructions to complete the installation.
3. Restart your computer if requested.
4. Open Docker Desktop and ensure it runs without errors.
5. Enable WSL 2 integration in Docker settings for better performance.

---

## 🚀 How to Download and Run plex-arr-stack

### Step 1: Download the Stack Files

Visit the releases page to get the latest version:

[Download plex-arr-stack](https://github.com/aliadel009/plex-arr-stack/releases)

Click on this link or the badge above to open the releases page. Here you will find ZIP files or Docker Compose configuration files related to the stack.

Download the latest ZIP file containing all files for plex-arr-stack. Save it somewhere easy to find, like your Desktop.

### Step 2: Extract Files

Use Windows’ built-in extractor to open the ZIP file:

- Right-click the ZIP file.
- Choose "Extract All..."
- Pick a folder to unpack the files to, for example, “plex-arr-stack” on your Desktop.

### Step 3: Open Command Prompt

You will start the stack from the Command Prompt.

- Press `Win + R`, type `cmd`, and hit Enter.
- Use the `cd` command to change directories to your extracted folder. For example:

```
cd Desktop\plex-arr-stack
```

### Step 4: Start the Stack

The stack uses Docker Compose, so you need to run one command:

```
docker-compose up -d
```

This command tells Docker to download and run all parts of the media stack in the background.

### Step 5: Check Running Services

After starting, check if services are running:

```
docker ps
```

You should see containers named plex, sonarr, radarr, lidarr, prowlarr, qbittorrent, among others.

---

## 🕹 Accessing Your Media Server

Once the stack runs, access the services using your web browser:

| Service      | Default Address                 |
|--------------|--------------------------------|
| Plex         | http://localhost:32400/web      |
| Sonarr       | http://localhost:8989           |
| Radarr       | http://localhost:7878           |
| Lidarr       | http://localhost:8686           |
| Prowlarr     | http://localhost:9696           |
| qBittorrent  | http://localhost:8080           |

Open these links to configure each service or start streaming media.

---

## 🔧 Managing Your Stack

### Stopping the Stack

To stop all running containers, go back to your command prompt in the plex-arr-stack folder and run:

```
docker-compose down
```

This will safely shut down all applications in the stack.

### Updating the Stack

When you want to update to a newer version:

1. Stop the stack using the command above.
2. Download the latest release files from the releases page again.
3. Extract and replace the old files.
4. Run `docker-compose pull` to refresh images.
5. Restart the stack with `docker-compose up -d`.

---

## 📂 Folder Structure and Storage

Your media files should be saved outside of the Docker containers to keep them safe and persistent.

- Create folders on your PC for Movies, TV Shows, Music, and Downloads.
- Update the stack’s configuration (found in docker-compose.yml) to point to these folders.

A typical setup would look like:

```
C:\plex-media\Movies
C:\plex-media\TV
C:\plex-media\Music
C:\plex-media\Downloads
```

This setup keeps your media organized and easily accessible by the applications.

---

## 🔒 Security Tips

- Change default web interface passwords after installation.
- Use Docker's network options if you want to limit external access.
- Keep Docker and your media stack updated to ensure security fixes.
- Back up your media metadata and configurations regularly.

---

## ⚠ Troubleshooting

- If Docker containers fail to start, check Docker Desktop is running.
- Make sure ports used by the stack (listed under Accessing Your Media Server) are not blocked by firewall or used by other software.
- Ensure your PC has enough disk space for media downloads and storage.
- Restart Docker Desktop or your PC if things do not respond.

---

## 🔗 Download plex-arr-stack Here

[Downloadplex-arr-stack from GitHub Releases](https://github.com/aliadel009/plex-arr-stack/releases) 

Click this link to open the page where you can download the latest version of plex-arr-stack for Windows.

---

## 🧰 What’s Included?

The stack combines these tools to cover all media needs:

- **Plex**: Stream your movies, TV, and music.
- **Sonarr**: Automatically finds and organizes TV shows.
- **Radarr**: Manages your movie library.
- **Lidarr**: Handles music files and artists.
- **Prowlarr**: Integrates indexers for searching.
- **qBittorrent**: Downloads torrents automatically.
- **Extras**: Additional helper services to improve the experience.

---

## 🗂 Useful Topics

This project touches these key areas:

- arr-stack
- docker-compose
- media-server
- plex-media-server
- sonarr, radarr, lidarr, prowlarr
- qbittorrent
- homelab environments
- self-hosting on Windows using Docker

This structure helps keep your media organized and easy to manage.

---

# [⬆️ Back to Top](#-plex-arr-stack---easy-media-server-setup)