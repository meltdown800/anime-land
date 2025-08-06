# 🌐 Anime Site - Docker Setup

A simple static website hosted inside a Docker container using **nginx** on an **Ubuntu Server** VM.
This is just a test and won't be extended anymore. 

---

## Project Structure
/srv/docker/anime-site/
├── html/ # Website source files (HTML/CSS)
├── docker/ # Dockerfile and image build context
│ └── Dockerfile
└── README.md # This documentation


## Docker Images

| Tag              | Description                              |
|------------------|------------------------------------------|
| `anime-site:prod` | Production image with static site copied inside |
| `anime-site:dev`  | Development image using bind mount (live updates) |

---

## Run Instructions

### Development (live-edit):

```bash
docker run -d \
  --name anime-dev \
  -p 8080:80 \
  -v /srv/docker/anime-site/html:/usr/share/nginx/html:ro \
  nginx:stable
