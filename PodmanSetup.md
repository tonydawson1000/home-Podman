# Podman Setup
[Home](ReadMe.md)
## Description
---
Document to show the basic Podman setup and usage controls.

## Podman Setup
---
Podman allows you to create a locally running Linux VM to run Podman.

The first step is initialising and managing a new VM using the `podman machine` commands.

## Podman Machine
---
| Command                   | Description |
| ---                       | --- |
| `podman machine`          | View Options |
| `podman machine init`     | Initialise a new VM |
| `podman machine list`     | View any existing Podman VMs |
| `podman machine info`     | View Podman Machine info / status |
| `podman machine start`    | Start an existing machine |
| `podman machine stop`     | Stop an existing machine |
| `podman machine rm`       | Remove a 'stopped' machine |

## Podman System
---
| Command                   | Description |
| ---                       | --- |
| `podman system`           | View Options |
| `podman system info`      | Display podman system information |
| `podman system df`        | Show podman disk usage |

## Summary
---
To confirm your installation of Podman has been successful - run the following commands and verify the output.

If you havent already:

    podman machine init

    podman machine start

Pull and Run a 'simple' - short-lived image:

    podman run quay.io/podman/hello


Pull and Run a 'simple' - long-lived image - and test Ports:

    podman run -it -p 8080:80 nginx

Find the IP assigned to the Linux subsystem by Windows

    ip addr | grep 172 

Test the Workload (in this case nginx) - view the logs/requests when hitting the endpoint

    http://172.x.x.x:8080

Tidyup (Optional)

    podman machine stop

