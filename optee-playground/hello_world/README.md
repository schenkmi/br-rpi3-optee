# Simple OP-TEE hello world example

## Build instructions
After build the RPI3 Buildroot stuff

Prepare
```
export BR_HOME=/build
export BR_OUTPUT=$BR_HOME/out/
export BR_HOST_BIN=$BR_OUTPUT/host/bin
export BR_SYSROOT=$BR_OUTPUT/host/aarch64-buildroot-linux-gnu/sysroot
```

Build example with
```
cd $BR_HOME/br-rpi3-optee/optee-playground/hello_world
PATH=$BR_HOST_BIN:$PATH TA_DEV_KIT_DIR=$BR_SYSROOT/ta_dev_kit CROSS_COMPILE=aarch64-linux-gnu- make
```

Clean example with
```
cd $BR_HOME/br-rpi3-optee/optee-playground/hello_world
PATH=$BR_HOST_BIN:$PATH TA_DEV_KIT_DIR=$BR_SYSROOT/ta_dev_kit CROSS_COMPILE=aarch64-linux-gnu- make clean
```
