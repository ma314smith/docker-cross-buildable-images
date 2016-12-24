# docker-cross-buildable-images
Images that can be built cross-architecture (build ARM images on the docker hub)

This uses the technique described in https://resin.io/blog/building-arm-containers-on-any-x86-machine-even-dockerhub/

## Images

- [ma314smith/rpi2-python-qemu](https://hub.docker.com/r/ma314smith/rpi2-python-qemu)
- [ma314smith/rpi2-node-qemu](https://hub.docker.com/r/ma314smith/rpi2-node-qemu)

## Cross Building
Reference one of the cross-buildable base images, and then use `cross-build-start` and `cross-build-end` around your normal docker commands

>FROM ma314smith/rpi2-python-qemu

>RUN [ "cross-build-start" ]

>// your normal docker commands

>RUN [ "cross-build-end" ]
