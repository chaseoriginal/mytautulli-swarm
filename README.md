# mytautulli-swarm

Plex statistics and monitoring for myplex server.

## Stack

- **Host**: ore-dock-110-1
- **Stack**: `mytautulli-swarm`
- **Image**: lscr.io/linuxserver/tautulli:latest
- **Config**: named volume `mytautulli-swarm.config`

## Ports

| Port | Published | Protocol |
|------|----------|----------|
| 8181 | 83 | TCP |

## Deploy

```bash
ssh ore-dock-110-1
cd /data/compose/mytautulli-swarm
set -a && source .env && docker stack deploy -c docker-compose.yml --with-registry-auth mytautulli-swarm && set +a
```
