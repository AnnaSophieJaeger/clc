# CLC Project - Bukkit Server
## Summary
The goal is a fully automated Minecraft server running with Bukkit. The challenges faced are that Bukkit is not distributed as an executeable. 
Instead, only the source code is available and the software must be compiled each time a new release happens. Therefore, a webhook or cron job must monitor the codebase and trigger a buildjob which builds a new image whenever an update arrives.
This update must then be deployed to the running server instance without major service interruption.
Additional care has to be taken for plugins, these must also be kept updated without them being integrated into the image itself; plugins may create additional files which should not be lost when restarting or updating the Bukkit version.
Also, minecraft worlds should be persisted and a backup made regularly.

## What is Bukkit?
Bukkit is an community build, open source Minecraft server. It differs from the default Minecraft server in that it offers an API to develop plugins for the Minecraft server.
This allows people to alter gameplay on the server in ways not possible on the vanilla Minecraft server.
Additional administration plugins also make the lives of server operators easier.
The downside to the vanilla Minecraft server is that the Bukkit executable is not available to download to due a DCMA takedown. The server code however is available plus there are build tools offered by the developers to easily compile and deploy Bukkit.

