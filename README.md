# `avahi-tools` Docker Image

Docker image for the `avahi-tools` to communicate (as a client) with the `avahi-daemon` running on docker host. Built on Alpine Linux to make the image as small as possible.

## Usage

Basic usage consists of running the docker container, mapping the required directories (`dbus` and `avahi-daemon` directory) to communicate with the `avahi-daemon` and calling one of the `avahi-*` commands to achieve your desired behaviour.

```shell
docker run -v /run/dbus:/var/run/dbus -v /run/avahi-daemon:/var/run/avahi-daemon --nework host ahasbini/avahi-tools:latest avahi-publish-service -s machine_hostname _ssh._tcp 2222
```
