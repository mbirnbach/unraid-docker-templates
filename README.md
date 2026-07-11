# Unraid Docker Templates

This repository contains custom Unraid Community Applications (CA) templates for personal or shared use.  
Each template allows you to easily deploy and configure Docker containers via the Unraid web UI without manual setup.

---

## 📦 Included Templates

### 🖼️ Plex Overlay
**Description**: Self-contained webhook + image server that displays "Now Playing" Plex posters — perfect for use with dashboards like DAKboard or hallway displays.

- Webhook URL: `http://[IP]:8080/webhook`
- Static image: `http://[IP]:8081/now-playing.png`
- Ports: 8080 (webhook), 8081 (image)
- Configurable via environment variables
- No volumes required

GitHub: [https://github.com/mbirnbach/plex-overlay](https://github.com/mbirnbach/plex-overlay)  
Docker Hub: [https://hub.docker.com/r/mbirnbach/plex-overlay](https://hub.docker.com/r/mbirnbach/plex-overlay)

---

### 🖥️ Hallway Dashboard
**Description**: Self-hosted, always-on wall-display dashboard for a hallway/kitchen TV (portrait orientation). Clock, weather + 6-day forecast, sunrise/sunset, indoor temp/humidity (Home Assistant), a rolling 4-week calendar (personal + waste/bin collection), a NINA/BBK civil-protection alert banner, a monthly background photo, and a random joke. Every field is optional and degrades gracefully.

- Web UI: `http://[IP]:8080/`
- Ports: 8080 (web UI)
- Configurable via environment variables (weather location, ICS calendar URLs, AGS code, Home Assistant, clock format, accent color)
- Volume: `backgrounds` folder for monthly background photos (`01.jpg` … `12.jpg`)

GitHub: [https://github.com/mbirnbach/hallway-dash](https://github.com/mbirnbach/hallway-dash)  
Docker Hub: [https://hub.docker.com/r/mbirnbach/hallway-dash](https://hub.docker.com/r/mbirnbach/hallway-dash)

---

## 🧰 How to Use This Repo in Unraid

1. In the Unraid web UI, go to **Apps > Settings**
2. Under **"Add Template Repository"**, enter:
   ```
   https://github.com/mbirnbach/unraid-docker-templates
   ```
3. Click **Apply**, then refresh the **Apps** tab
4. You’ll see your custom templates appear — ready to install like any other app

---

## 🛠 Structure

```
/templates/         # XML templates for each app
/icons/             # Icons shown in the CA app store
README.md           # You're here
```

---

## 🧪 Adding New Templates

To add a new container:

1. Duplicate an existing XML in `/templates/`
2. Modify:
   - `<Name>`
   - `<Repository>`
   - `<Overview>` and `<Description>`
   - `<Environment>` and `<Port>` mappings
3. Add a PNG icon to `/icons/` (128x128 recommended)
4. Update this `README.md` to include your new app

---

## 🧑‍💻 Maintainer

This repo is maintained by **mbirnbach**.  
If you'd like to reuse, fork, or contribute templates — feel free!

