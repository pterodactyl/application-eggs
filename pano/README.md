# [Pano](https://panomc.com)

Open-source web platform for Minecraft servers: website, web store and management panel in one.
Source: <https://github.com/PanoMC/Pano>, docs: <https://panomc.com/docs/>.

## Setup

1. Create a server with the egg (Java 11 or newer, Java 21 recommended).
2. Optional: create a database (MariaDB / MySQL) and fill the database variables. They are read on the
   first start only; left empty, the setup wizard asks for the database.
3. Start the server, browse to `http://<ip>:<port>` and finish the setup wizard.

A reinstall upgrades Pano to `PANO_VERSION` (or the newest release of `PANO_CHANNEL`) and keeps all data.
Updating from Pano's own panel works too: Pano installs the new version and exits, the panel restarts it.

## Server Ports

Pano needs 1 port, the web port (HTTP). Any port works.

| Port | default |
|------|---------|
| Web  | 8088    |

## Memory

1 GB is enough for a small site: the JVM gets half of it (`JAVA_RAM_PERCENT`), the other half is left to the
website processes Pano runs next to it (setup, panel and theme). Use 1.5 GB or more for busy sites.
