# [ccio-openwrt-builder](https://hub.docker.com/r/containercraft/ccio-openwrt-builder)
Builder image for ccio-openwrt lxd image

###### Example Usage:
```
mkdir /tmp/openwrt
sudo podman run --privileged --rm -it --name openwrt_builder --volume /tmp/openwrt:/root/bin:z containercraft/ccio-openwrt-builder:19.07.2
lxc image import /tmp/openwrt/openwrt-19.07.2-x86-64-lxd.tar.gz --alias openwrt/19.07.2/x86_64
```

###### Refrence:
[ccio-openwrt](https://github.com/containercraft/ccio-openwrt)    
[OpenWRT Releases](https://openwrt.org/releases/start)    
[Podman.io](https://podman.io/getting-started/installation)    
