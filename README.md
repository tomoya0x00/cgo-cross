# cgo-cross

cgo-crsoss is cross compiling toolchains for cgo in Docker images.

[Docker Hub](https://hub.docker.com/r/tomoya0x00/cgo-cross/)

## linux-arm

Usage:

```bash
cd YourSrcDir
docker run --rm -v "$PWD":/go/src/YourAppName -w /go/src/YourAppName tomoya0x00/cgo-cross:1.8.0-linux-arm go build -v
```
