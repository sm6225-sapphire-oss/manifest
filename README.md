# Build guide

1. Initialize and sync firmware repo
2. Clone device tree
   (It is recommended to use [ssh](./ssh.md))

```sh
git clone -b 15 --depth 1 https://github.com/sm6225-sapphire-oss/device_xiaomi_sapphire.git device/xiaomi/sapphire
```

3. Clone kernel tree

```sh
git clone -b 15 --depth 1 https://github.com/sm6225-sapphire-oss/device_xiaomi_sapphire-kernel.git device/xiaomi/sapphire-kernel
```

4. Clone vendor tree

```sh
git clone -b 15 --depth 1 https://github.com/sm6225-sapphire-oss/vendor_xiaomi_sapphire.git vendor/xiaomi/sapphire
```

5. Replace stock components with components from our repositories

```sh
rm -rf device/qcom/sepolicy_vndr/sm6225
git clone -b 15 --depth 1 https://github.com/sm6225-sapphire-oss/device_qcom_sepolicy_vndr.git device/qcom/sepolicy_vndr/sm6225

rm -rf hardware/qcom-caf/common
git clone -b 15 --depth 1 https://github.com/sm6225-sapphire-oss/hardware_qcom-caf_common.git hardware/qcom-caf/common

rm -rf hardware/qcom-caf/sm6225/audio/agm
git clone -b 15 --depth 1 https://github.com/sm6225-sapphire-oss/vendor_qcom_opensource_agm.git hardware/qcom-caf/sm6225/audio/agm

rm -rf hardware/qcom-caf/sm6225/audio/pal
git clone -b 15 --depth 1 https://github.com/sm6225-sapphire-oss/vendor_qcom_opensource_arpal-lx.git hardware/qcom-caf/sm6225/audio/pal

rm -rf hardware/qcom-caf/sm6225/audio/primary-hal
git clone -b 15 --depth 1 https://github.com/sm6225-sapphire-oss/hardware_qcom_audio-ar.git hardware/qcom-caf/sm6225/audio/primary-hal

rm -rf hardware/qcom-caf/sm6225/data-ipa-cfg-mgr
git clone -b 15 --depth 1 https://github.com/sm6225-sapphire-oss/vendor_qcom_opensource_data-ipa-cfg-mgr.git hardware/qcom-caf/sm6225/data-ipa-cfg-mgr

rm -rf hardware/qcom-caf/sm6225/dataipa
git clone -b 15 --depth 1 https://github.com/sm6225-sapphire-oss/vendor_qcom_opensource_dataipa.git hardware/qcom-caf/sm6225/dataipa

rm -rf hardware/qcom-caf/sm6225/display
git clone -b 15 --depth 1 https://github.com/sm6225-sapphire-oss/hardware_qcom_display.git hardware/qcom-caf/sm6225/display

rm -rf hardware/qcom-caf/sm6225/media
git clone -b 15 --depth 1 https://github.com/sm6225-sapphire-oss/hardware_qcom_media.git hardware/qcom-caf/sm6225/media

rm -rf device/xiaomi/sepolicy
git clone --depth 1 https://github.com/sm6225-sapphire-oss/device_xiaomi_sepolicy.git device/xiaomi/sepolicy

rm -rf hardware/xiaomi
git clone --depth 1 https://github.com/sm6225-sapphire-oss/hardware_xiaomi.git hardware/xiaomi
```

6. Include MiuiCamera (optional)

```sh
rm -rf device/xiaomi/miuicamera-sapphire
git clone --depth 1 https://github.com/sm6225-sapphire-oss/device_xiaomi_miuicamera-sapphire.git device/xiaomi/miuicamera-sapphire

rm -rf vendor/xiaomi/miuicamera-sapphire
git clone --depth 1 https://gitlab.com/ReStranger/vendor_xiaomi_miuicamera-sapphire.git vendor/xiaomi/miuicamera-sapphire
```

7. Build rom!!!
8. Fix bug, include productivity and contribute to the overall project!!!

# Credits and thanks

- [kibria5](https://github.com/kibria5)
