# Simple multi subdomain vps (hetzner), caddy & cloudflare server

## Caddy folder
This has the configuration to run a caddy socker compose configured to have https dns auto config

Inside certs folder you must put the origin certificates (cert & private key)

Go to [github page](https://github.com/lucaslorentz/caddy-docker-proxy) for more info.

## Cloudflared folder
This one has the docker compose for connect a cloudflare tunnel

More instructions found in [coolify page](https://coolify.io/docs/knowledge-base/cloudflare/tunnels/full-tls).

## Whoami folder
This has a simple service example to mount


## How to run
Having docker compose installed in the system just is needed to run `docker compose up -d` inside each of the folders.

```bash
docker compose up -d
```

The sugested order might be:
- cloudflared (check if tunnel is healthy)
- caddy
- whoami (test if is accesible with the dns)

