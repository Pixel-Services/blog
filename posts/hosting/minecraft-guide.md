---
title: "Minecraft Hosting Guide"
description: "A comprehensive guide on hosting and managing your Minecraft server with us."
---

## Types of Servers

There are three main types:

- **Vanilla**: Unmodified, official server software. No plugin/mod support.
- **Plugins**: Requires platforms like Spigot, Paper, or Purpur. Adds server-side customizations.
- **Mods**: Requires Forge or Fabric. Clients must use the same modpack.

## Proxy Servers

A proxy (e.g., Velocity, BungeeCord) links multiple backend servers under one IP. Used for network-based setups (e.g., lobby → survival). Each sub-server requires its own slot and configuration.

## RAM Allocation

RAM affects performance, especially with plugins, players, or large worlds. Our servers use **DDR5** memory for optimal speed and latency. Select the RAM amount based on your expected usage.

## Server Types

We support and preconfigure:

- **Spigot**: Basic plugin support, good performance.
- **Paper**: Performance-enhanced Spigot fork, most recommended.
- **Purpur**: Adds additional features and patches over Paper.
- **Folia**: Experimental multi-threaded fork, use with caution.
- All types can be selected in the software menu during server setup.

## Console and Commands

The console allows you to execute commands as server operator. Basic commands include:

- `/stop`: stops the server.
- `/op <player>`: grants operator rights.
- `/tp <a> <b>`: teleports players.

Plugins may introduce additional commands, listed in their respective documentation.

## File Structure Overview

- **server.properties**: General settings (difficulty, MOTD, player slots).
- **/plugins**: Plugin `.jar` files and configs.
- **/world**, **/world_nether**, **/world_the_end**: Default generated worlds.
- **/config**, **/logs**, **/mods** (if modded): Vary by server type.

## Schedules

Automated tasks (e.g., restarts, commands) can be defined through the schedule system in your panel.

## Backups

We provide **2 offsite backups** by default. Offsite means stored externally from your main server node, increasing data resilience in case of failure or attack.

## Networking

Each server includes **5 open ports** (1 primary + 4 auxiliary) to allow flexibility for proxies, plugin APIs, or mod integration.

## Database Access

Up to **5 MySQL databases** per server. Connection details (host, user, password, port) are provided in the interface. Use these credentials to connect from your server or external tools.

## Security Notes

- We run a **honeypot system** to detect and block scanner bots at the infrastructure level.
- This is a mitigation layer, **not full protection**.
- For private communities, enable a whitelist.
- For servers with `online-mode=false`, use an authentication plugin to prevent unauthorized access.

