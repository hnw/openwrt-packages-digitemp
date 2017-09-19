# openwrt-packages-digitemp

This is `digitemp` package for LEDE, tested on 17.01.2 .

# How to install binary package

```
$ opkg update
$ opkg install openssl-util
$ echo 'src/gz hnw https://dl.bintray.com/hnw/openwrt-packages/15.05.1/ar71xx' >> /etc/opkg/customfeeds.conf
$ opkg update
$ opkg install digitemp
```

# How to build

To build these packages, add the following line to the feeds.conf in the OpenWrt buildroot:

```
$ echo 'src-git hnw_digitemp https://github.com/hnw/openwrt-packages-digitemp.git' >> feeds.conf
```

Then you can build packages as follows:

```
$ ./scripts/feeds update -a
$ ./scripts/feeds install digitemp
$ make packages/digitemp/compile
```
