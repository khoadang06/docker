FROM caddy:builder AS builder

RUN xcaddy build \
    --with github.com/caddy-dns/cloudflare \
    --with github.com/mholt/caddy-l4

FROM caddy:builder

COPY --from=builder /usr/bin/caddy /usr/bin/caddy