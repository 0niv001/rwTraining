---
sticker: lucide//box
---
Allows for a standardised way to package and run apps, so that apps can run anywhere regardless of the dev environment. 

First we package the app as an image {Containerisation}, and then we run it as a container.

Container is an isolated execution environment, standardising process of running any service in local user or dev environment. 

**Difference with VM**

| Docker                                       | VM                              |
| -------------------------------------------- | ------------------------------- |
| Docker images are smaller                    | VM Images are larger            |
| Containers are faster to start               | VMs are slower due to boot up   |
| Docker is compatible with only Linux distros | VMs are compatible with all OSs |

Steps from app to container:
- Develop
- Build app and dependencies into img
- Ship image to registry (optional)
- Run as container

**Docker Images**
- Source code
- Libraries
- System tools
- Settings

**Registries**
- Can be managed using docker CLI or web interface provided by registry provider

| Public                                                         | Private                                                                             |
| -------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| Anyone can store and share images                              | Restricted to specific users or organisations                                       |
| Docker Hub Google Container Registry, Amazon elastic container | More secure way to store distributed images                                         |
|                                                                | Used for custom or proprietary software                                             |
|                                                                | Can cache images downloaded from public registries, reducing network data transfers |
|                                                                |                                                                                     |
**Docker file use cases**
- Creating dev environment
- Creating a production ready image
- Versioning and collaboration
- Testing and [[CICD]]

Image is made up of layers and can be used to start one or more containers. 

Registries are places to store and retrieve images. 

Storing and retrieving images is pushing and pulling,
## Commands
```
docker build -> builds an image 

docker build -t {image-name}. -f Dockerfile -> create image with dockerfile 

docker run --name {container-name} {image-name}



docker push {link}

docker pull {link}

docker start [container id]
docker stop [container id]

exec {Use to access container}
```

## Dockerfile