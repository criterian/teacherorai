# Teacher or AI?

Four-round workshop game for the SMART-AI4Assessment learning activity (Zaragoza, 2026).
Static single page served by nginx. No backend, no database, no student data on the server:
game state and edited content are kept in the facilitator's browser (localStorage).

## Deploy on Coolify
1. Push this folder to a Git repository (GitHub/GitLab/Gitea).
2. Coolify → Project → + New → Application → (Public or Private) Repository.
3. Build pack: **Dockerfile**. Base directory: `/`. Ports exposes: `80`.
4. Domains: `https://game.example.org` (DNS A record → your Coolify server IP).
5. Deploy. Health check path: `/healthz`.

## Run locally
    docker build -t teacher-or-ai .
    docker run --rm -p 8080:80 teacher-or-ai
    # open http://localhost:8080
