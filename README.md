# TWRP device tree for OPLUS ossi

## Supported devices

- OnePlus Pad 2 Pro

## Build it yourself?

```shell
mkdir twrp && cd twrp
repo init --depth=1 -u https://github.com/TWRP-Test/platform_manifest_twrp_aosp.git -b twrp-16.0
repo sync
git clone --depth=1 https://github.com/AuroraRecoveryProject/twrp_device_oplus_ossi device/oplus/ossi
```

```shell
source build/envsetup.sh
lunch twrp_ossi
m rrecoveryimage
```

If there is no error, recovery.img will be found in `out/target/product/ossi/recovery.img`

## Features

Works:

- [X] ADB
- [X] Display
- [X] Decryption
- [X] Fasbootd
- [X] Flashing
- [X] MTP
- [X] Sideload
- [X] Touch
- [X] USB OTG
- [x] WLAN(OEM)
- [ ] Vibrator(OnePlus Pad have no vibrator, so it is not tested)

## To use it

```shell
fastboot flash recovery recovery.img
```

or

```shell
fastboot flash recovery_a recovery.img
fastboot flash recovery_b recovery.img
```
