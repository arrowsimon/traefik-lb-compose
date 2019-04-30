docker network create reverse-proxy
touch acme.json && chmod 600 acme.json

admin / admin

labels:
      - "traefik.enable=true"
      - "traefik.frontend.rule=Host:<HOSTNAME>"
      - "traefik.port=<EXPOSE PORT>"
      - "traefik.docker.network=reverse-proxy"
