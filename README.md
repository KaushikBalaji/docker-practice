# C Calculator App [(Dockerized)](https://hub.docker.com/r/kaushikbalaji/calci-app/tags)

This repository contains a simple C-based calculator application packaged as a Docker image.

The image is hosted on Docker Hub and can be pulled and run by anyone.

The docker image is at https://hub.docker.com/r/kaushikbalaji/calci-app/tags

## 🚀 Quick Start: Run the App from Another machine

If you just want to run the calculator app, you don't need to build it. You can pull the pre-built image directly from Docker Hub.

### 1. Pull the Image and run with a container

Open your terminal and pull the versioned image, and run the image in a container. This will run the app:

```bash
docker pull kaushikbalaji/calci-app:1.0

# to create a nameless container: it opens, runs the app and closes itself.
docker run -it --rm kaushikbalaji/calci-app:1.0

# if u want to have a single container, then name it, and reuse it.
docker run -it --name calci_container kaushikbalaji/calci-app:1.0
```

## 🛠️ How This Was Built
### 1. Build the Image

The image was built locally using the Dockerfile in this repository.
```bash
# Build the image and tag it
sudo docker build -t kaushikbalaji/calci-app .

# for local testing of image
sudo docker run -it --rm kaushikbalaji/calci-app:latest

# make a new image with tag for pushing
sudo docker tag kaushikbalaji/calci-app kaushikbalaji/calci-app:1.0

# Push the new 1.0 tag image to Docker Hub
sudo docker push kaushikbalaji/calci-app:1.0
```
## Some screenshots

### File strcture
<img width="1920" height="1080" alt="file structure" src="https://github.com/user-attachments/assets/7795938d-28e6-4379-965a-31eef124d00f" />

### Docker image building
<img width="1920" height="1080" alt="docker image build" src="https://github.com/user-attachments/assets/21ae3d54-ce0f-4cf9-a4dd-c475e57be7ef" />

### Running with container
<img width="1512" height="719" alt="container running" src="https://github.com/user-attachments/assets/520ed2e4-4ebf-44ae-8b05-49530decd9e2" />

### Docker image pushed to DockerHub
<img width="1915" height="1043" alt="after push to docker" src="https://github.com/user-attachments/assets/a7ff4617-6784-4044-8996-5cfaad0b5afa" />

### Pulled the image and ran it on another machine (with windows OS)
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/c8d93ab4-aa57-4279-ad0b-01e1055b8e0c" />

### Docker run works on another windows system
<img width="1600" height="850" alt="image" src="https://github.com/user-attachments/assets/ad60f678-8175-4ed0-8a59-029a9d6b1c5a" />





