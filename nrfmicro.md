hex bootloader to patch
https://github.com/joric/nrfmicro/releases/download/1.4/pca10056_bootloader-0.5.0-dirty_s140_6.1.1.hex


## Blackmagic on st-link v2

firmware https://github.com/sakana280/stlink-tool/releases/download/1.0-Win64/blackmagic.bin
tool https://github.com/UweBonnes/stlink-tool/tree/stlinkv21

command for flashing bootloader in st-link v2

```
./stlink-tool ../../Downloads/blackmagic.bin
```

Docker command for flashing nrfmicros:
```
docker run --rm -it --privileged --device=/dev/ttyACM0 --name nrfconnect-sdk -v ${PWD}:/workdir/project stronglytyped/arm-none-eabi-gcc /bin bash

arm-none-eabi-gdb --batch -ex "target extended-remote /dev/ttyACM0" -ex "mon swdp_scan" -ex "file bootloader.hex" -ex "att 1" -ex "mon erase" -ex load

```