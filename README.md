# agentring-dokploy

Despliegue de [agentring](https://github.com/mutonby/agentring) (relay + LiveKit) en Dokploy.

- `relay/` — fuente del relay, copiado de `mutonby/agentring` (Apache-2.0). Las imágenes
  precompiladas de GHCR del proyecto **no son públicas**, así que aquí se construye desde
  fuente.
- `docker-compose.yml` — relay + LiveKit con **7881/tcp y 50000-50100/udp publicados**
  (el audio de las llamadas) y Traefik en la red `dokploy-network`.

Las variables se definen en Dokploy > Environment (no hay secretos en este repo).
