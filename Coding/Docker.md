---
sticker: lucide//box
---
Allows for a standardised way to package and run apps, so that apps can run anywhere regardless of the dev environment. 

First we package the app as an image {Containerisation}, and then we run it as a container.
Container is an isolated execution environment. 

Benefits over VMs:
- Smaller
- Faster
- Portable

Steps from app to container:
- Develop
- Build app and dependencies into img
- Ship image to registry (optional)
- Run as container

Image is made up of layers and can be used to start one or more containers. 

Registries are places to store and retrieve images. 

Storing and retrieving images is pushing and pulling,
## Commands
```docker
docker build -> builds an image 

docker build -t {image-name}. -f Dockerfile -> create image with dockerfile 

docker run --name {container-name} {image-name} 

docker push {link}

docker pull {link}
```