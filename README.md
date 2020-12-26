# minecraft-server

Target for ubuntu 20

### Commands (as root)
- `mkdir /opt/minecraft`
- `useradd minecraft`
- `wget -O /opt/minecraft/server.jar https://launcher.mojang.com/v1/objects/35139deedbd5182953cf1caa23835da59ca3d7cd/server.jar` 
  - from: https://www.minecraft.net/en-us/download/server
- `wget -O /opt/minecraft/spigot.jar https://cdn.getbukkit.org/spigot/spigot-1.16.4.jar` 
  - from https://getbukkit.org/get/MvbtKzCMFRVUPyKHvZ0cmiThXiiTSe92
- `apt-get update`
- `apt-get install openjdk-8-jdk`
- `java -Xmx3800M -Xms3800M -jar spigot.jar nogui` (accept eula and restart)
- `mkdir /opt/minecraft/plugins`
- `wget -O /opt/minecraft/plugins/miencraft-prometheus-exporter-2.2.0.jar https://github.com/sladkoff/minecraft-prometheus-exporter/releases/download/v2.2.0/minecraft-prometheus-exporter-2.2.0.jar`
  - from https://github.com/sladkoff/minecraft-prometheus-exporter/releases/tag/v2.2.0
