# C Calculator App [(Dockerized)](https://hub.docker.com/r/kaushikbalaji/calci-app/tags)

This repository contains a simple C-based calculator application packaged as a Docker image.

The image is hosted on Docker Hub and can be pulled and run by anyone.

The docker image is at https://hub.docker.com/r/kaushikbalaji/calci-app/tags

## 🚀 Quick Start: Run the App from Another machine

If you just want to run the calculator app, you don't need to build it. You can pull the pre-built image directly from Docker Hub.

### 1. Pull the Image

Open your terminal and pull the versioned image, and run the image in a container. This will run the app:

```bash
docker pull kaushikbalaji/calci-app:1.0

# to create a nameless container: it opens, runs the app and closes itself.
docker run -it --rm kaushikbalaji/calci-app:1.0
```

If you want to run the container and have it persist (not be removed) after you exit, you can give it a name.
```bash
docker pull kaushikbalaji/calci-app:1.0

# Run and name the container
docker run -it --name calci_container kaushikbalaji/calci-app:1.0

# After you exit, the container will be stopped. You can see it with:
docker ps -a

# To restart and re-attach to the same container:
docker start -i calci_container
```


## 🛠️ How This Was Built
### 1. Build the Image

The image was built locally using the Dockerfile in this repository.
```bash
# Build the image and tag it
sudo docker build -t kaushikbalaji/calci-app .
```

### 2. Test Locally

Before publishing, the image was run locally to ensure the calculator app worked as expected.

```bash
# Run interactively, and remove the container after exit
sudo docker run -it --rm kaushikbalaji/calci-app:latest
```

### 3. Tag for Release

After successful testing, the latest image was given a specific version tag (1.0). This is a best practice for version control.
```bash
# Tag the image with version 1.0
sudo docker tag kaushikbalaji/calci-app kaushikbalaji/calci-app:1.0
```

### 4. Publish to Docker Hub

Finally, the versioned image was pushed to the Docker Hub registry, making it publicly available for the docker pull command.
```bash
# Push the 1.0 tag to Docker Hub
sudo docker push kaushikbalaji/calci-app:1.0
```



