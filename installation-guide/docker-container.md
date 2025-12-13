# Docker Container

Holesail provides an official Docker image that allows you to run servers, clients, and the built-in file manager without installing Node.js or managing binaries manually.

Docker is the **recommended installation method** for:

* Headless servers (VPS, NAS, homelab)
* Production deployments
* Isolated or reproducible environments
* Easy upgrades and rollbacks

Requirements:

* Docker
* A system that supports host networking (Linux recommended)

Pull the docker image:

```bash
docker pull holesail/holesail:latest
```

### Server Mode

Runs a Holesail server that exposes a local service.

```
docker run -d --name holesail \
  -e MODE=server \
  -e PORT=25565 \
  -e HOST=127.0.0.1 \
  -e KEY=very-super-secret \
  -e PUBLIC=false \
  --network host \
  holesail:latest
```

### Client Mode

Connects to a remote Holesail server using its key.

```
docker run -d --name holesail-client \
  -e MODE=client \
  -e PORT=25565 \
  -e HOST=127.0.0.1 \
  -e KEY=very-super-secret \
  -e FORCE=true \
  -e LOG=true \
  --network host \
  holesail:latest
```

### File Manager Mode

Runs the Holesail file manager, allowing secure file access over P2P.

```
docker run -d \
  --name holesail-filemanager \
  -p 8080:8080 \
  -e MODE=filemanager \
  -e PORT=8080 \
  -e HOST=127.0.0.1 \
  -e PUBLIC=true \
  -e LOG=true \
  -e KEY=my-filemanager-key \
  -e FORCE=true \
  -e DIR=/app/files \
  -e USERNAME=admin \
  -e PASSWORD=securepass \
  -e ROLE=admin \
  -v /path/to/local/files:/app/files \
  holesail:latest
```

### Environment Variable Configuration

Holesail’s Docker image uses environment variables exclusively for configuration.\
The behavior is determined primarily by the `MODE` variable.

| Variable | Description                            |
| -------- | -------------------------------------- |
| `MODE`   | `server`, `client`, or `filemanager`   |
| `PORT`   | Local port to bind                     |
| `HOST`   | Bind address (default: `127.0.0.1`)    |
| `KEY`    | Connection key                         |
| `PUBLIC` | Allow public access (`true` / `false`) |
| `FORCE`  | Allow to use a short KEY               |
| `LOG`    | Enable logging                         |

File Manager Mode

| Variable   | Description              |
| ---------- | ------------------------ |
| `DIR`      | Directory to share       |
| `USERNAME` | Login username           |
| `PASSWORD` | Login password           |
| `ROLE`     | User role (e.g. `admin`) |

You can also define the flags above using a  `.env`  file if you choose to Docker compose instead of our existing image.
