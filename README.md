# minecraft-server

Target for ubuntu 20

### Set up the Server (as root)
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
- `wget -O /opt/minecraft/plugins/minecraft-prometheus-exporter-2.2.0.jar https://github.com/sladkoff/minecraft-prometheus-exporter/releases/download/v2.2.0/minecraft-prometheus-exporter-2.2.0.jar`
  - from https://github.com/sladkoff/minecraft-prometheus-exporter/releases/tag/v2.2.0
- `wget -O /opt/minecraft/plugins/geyser.jar https://ci.opencollab.dev/job/GeyserMC/job/Geyser/job/master/lastSuccessfulBuild/artifact/bootstrap/spigot/target/Geyser-Spigot.jar`
  - from: https://ci.opencollab.dev/job/GeyserMC/job/Geyser/job/master/
- !!Add your own plugins here!!
- `mkdir /opt/minecraft/logs
  
### Set up iptables
- `mkdir /opt/minecraft/scripts`
- `wget -O /opt/minecraft/scripts/iptables.sh https://raw.githubusercontent.com/james-m-tubbs/minecraft-server/main/iptables.sh`
- `chmod +x /opt/minecraft/scripts/iptables.sh`
- `/opt/minecraft/scripts/iptables.sh`

### Set up Node Exporter (optional)
- 

### Fix Permissions
- `chown -R minecraft:minecraft /opt/minecraft/

### Add Service

### Validation
hit server on:
- `:9225`
- `:9100`

