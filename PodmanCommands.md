# Podman Commands
[Home](ReadMe.md)
## Description
---
Document to show the basic Podman commands.

Assuming Podman has been setup and is running correctly - verify using :

    podman run quay.io/podman/hello 

## Podman Standard Commands
---
| Command                               | Description |
| ---                                   | --- |
| `podman version`                      | View Version |

## Podman Image (Build / Login / Push)
---
| Command                               | Description |
| ---                                   | --- |
| `podman build -t <image-name> .`      | Build an Image, using the Containerfile in current dir
| `podman images`                       | List images in local storage |
| `podman login quay.io`                | Login to Image Registry ([quay.io](https://quay.io/repository/)) |

## Podman Containers (List / Start / Stop)
---
| Command                               | Description |
| ---                                   | --- |
| `podman ps`                           | List 'running' containers |
| `podman ps -a`                        | List 'all' containers |
| `podman start <container-id>`         | Starts one or more containers.  |
| `podman stop <container-id>`          | Stops one or more running containers. |

## Podman 'Diagnostics'
---
| Command                               | Description |
| ---                                   | --- |
| `podman top <container-id>`           | Display the running processes of a container |
| `podman logs <container-id>`          | Retrieves logs for one or more containers |
| `podman inspect <container-id>`       | Display the low-level configuration of a container |
| `podman stats <container-id>`         | Display a live stream of container resource usage statistics (CPU/RAM/Network etc) |

## Podman 'Tidyup' (DESTRUCTIVE)
---
| Command                               | Description |
| ---                                   | --- |
| `podman rm`                           | Removes one or more containers from the host. |
| `podman rm -f $(podman ps -aq)`       | Removes ALL containers from the host. |
| `podman rmi -f $(podman images -aq)`  | Removes ALL images from the host. |
