# stm32cubeide

[stm32cubeide](https://github.com/xanderhendriks/docker-stm32cubeide): the STM32 Cube Integrated Development
Environment docker container.

## Build

To create the image `xanderhendriks/stm32cubeide`, execute the following command in the
`docker-stm32cubeide` folder:
```
docker build -t xanderhendriks/stm32cubeide .
```

## First Build

```bash
docker run -it \
--name stm32cubeide \
--device=/dev/bus/usb:/deb/bus/usb \
-v /home/parth/stm32cubeide/:/workspace \
-e DISPLAY=$DISPLAY \
-v /tmp/.X11-unix:/tmp/.X11-unix \
xanderhendriks/stm32cubeide
```

## Run

```bash
docker start stm32cubeide
docker exec -it stm32cubeide /bin/bash
```
