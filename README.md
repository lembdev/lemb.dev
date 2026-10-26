# lemb.dev

Root page of `lemb.dev` and the 404 page for unknown `*.lemb.dev` hosts.

- `public/`: static files, `nginx.conf`: server config (port 8080), image `ghcr.io/lembdev/lemb.dev`.
- Push to `main` builds the image and bumps the tag in `lembdev/homelab` (`k8s/apps/lemb-dev`), Argo CD deploys it to k3s.
- Local run: `docker build -t lemb.dev . && docker run --rm -p 8080:8080 lemb.dev`.
