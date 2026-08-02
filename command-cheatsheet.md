# 🐳 Docker Basic Commands Cheat Sheet

A quick reference for commonly used Docker commands.

---

# Create an Alias

Create a shortcut so you can use `d` instead of `docker`.

```bash
echo "alias d='docker'" >> ~/.bashrc
source ~/.bashrc
```

Verify:

```bash
d --version
```

---

# List Docker Images

Display all local Docker images.

```bash
docker images
```

or

```bash
docker image ls
```

---

# List All Images (Including Intermediate Images)

```bash
docker images -a
```

---

# Display Only Image IDs

```bash
docker images -q
```

---

# Inspect an Image

Display detailed information about an image.

```bash
docker inspect <image_id>
```

Example:

```bash
docker inspect 4abcf2066143
```

---

# Remove an Image

Delete a Docker image.

```bash
docker rmi <image_id>
```

Example:

```bash
docker rmi 4abcf2066143
```

---

# List Running Containers

```bash
docker ps
```

or

```bash
docker container ls
```

---

# List All Containers

Display both running and stopped containers.

```bash
docker ps -a
```

---

# Inspect a Container

Display detailed information about a container.

```bash
docker inspect <container_id>
```

Example:

```bash
docker inspect 8a7b6c5d4e3f
```

---

# Tag an Existing Image

Create a new tag for an existing image.

```bash
docker tag <image_id> <repository>:<tag>
```

Example:

```bash
docker tag 4abcf2066143 my-app:v1
```

Tag for Docker Hub:

```bash
docker tag my-app:v1 your_dockerhub_username/my-app:v1
```

---

# Login to Docker Hub

```bash
docker login
```

Logout:

```bash
docker logout
```

---

# Push an Image to Docker Hub

After tagging the image with your Docker Hub username:

```bash
docker push <dockerhub_username>/<image_name>:<tag>
```

Example:

```bash
docker push johndoe/my-app:v1
```

---

# Useful Commands

| Command | Description |
|----------|-------------|
| `docker --version` | Display Docker version |
| `docker images` | List Docker images |
| `docker ps` | List running containers |
| `docker ps -a` | List all containers |
| `docker inspect` | Display detailed information |
| `docker tag` | Create a new image tag |
| `docker push` | Upload an image to Docker Hub |
| `docker pull` | Download an image from Docker Hub |
| `docker rmi` | Remove an image |
| `docker rm` | Remove a container |
| `docker stop` | Stop a running container |
| `docker start` | Start a stopped container |

---

# References

- Docker CLI
- Docker Images
- Docker Containers
- Docker Hub

---

⭐ If you found this repository helpful, consider giving it a **Star**.