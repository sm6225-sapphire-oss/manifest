# Build guide

1. Initialize and sync firmware repo
2. Clone device tree

```sh
git clone -b 14.0 git@github.com:sm6225-sapphire-oss/device_xiaomi_sapphire.git device/xiaomi/sapphire
```

2. Clone vendor tree

```sh
git clone -b 14 git@github.com:sm6225-sapphire-oss/vendor_xiaomi_sapphire.git vendor/xiaomi/sapphire
```

3. Replace stock components with components from our repositories

```sh
rm -rf device/qcom/sepolicy_vndr/sm6225
git clone -b 14 --depth 1 git@github.com:sm6225-sapphire-oss/device_qcom_sepolicy_vndr.git device/qcom/sepolicy_vndr/sm6225

rm -rf hardware/qcom-caf/common
git clone -b 14 --depth 1 git@github.com:sm6225-sapphire-oss/hardware_qcom-caf_common.git hardware/qcom-caf/common

rm -rf hardware/qcom-caf/sm6225/audio/agm
git clone -b 14 --depth 1 git@github.com:sm6225-sapphire-oss/vendor_qcom_opensource_agm.git hardware/qcom-caf/sm6225/audio/agm

rm -rf hardware/qcom-caf/sm6225/audio/pal
git clone -b 14 --depth 1 git@github.com:sm6225-sapphire-oss/vendor_qcom_opensource_arpal-lx.git hardware/qcom-caf/sm6225/audio/pal

rm -rf hardware/qcom-caf/sm6225/audio/primary-hal
git clone -b 14 --depth 1 git@github.com:sm6225-sapphire-oss/hardware_qcom_audio-ar.git hardware/qcom-caf/sm6225/audio/primary-hal

rm -rf hardware/qcom-caf/sm6225/data-ipa-cfg-mgr
git clone -b 14 --depth 1 git@github.com:sm6225-sapphire-oss/vendor_qcom_opensource_data-ipa-cfg-mgr.git hardware/qcom-caf/sm6225/data-ipa-cfg-mgr

rm -rf hardware/qcom-caf/sm6225/dataipa
git clone -b 14 --depth 1 git@github.com:sm6225-sapphire-oss/vendor_qcom_opensource_dataipa.git hardware/qcom-caf/sm6225/dataipa

rm -rf hardware/qcom-caf/sm6225/display
git clone -b 14 --depth 1 git@github.com:sm6225-sapphire-oss/hardware_qcom_display.git hardware/qcom-caf/sm6225/display

rm -rf hardware/qcom-caf/sm6225/media
git clone -b 14 --depth 1 git@github.com:sm6225-sapphire-oss/hardware_qcom_media.git hardware/qcom-caf/sm6225/media

rm -rf device/xiaomi/sepolicy
git clone git@github.com:sm6225-sapphire-oss/device_xiaomi_sepolicy.git device/xiaomi/sepolicy

rm -rf hardware/xiaomi
git clone git@github.com:sm6225-sapphire-oss/hardware_xiaomi.git hardware/xiaomi
```

4. Include MiuiCamera (optional)

```sh
rm -rf device/xiaomi/miuicamera-sapphire
git clone -b 14 git@github.com:sm6225-sapphire-oss/device_xiaomi_miuicamera-sapphire.git device/xiaomi/miuicamera-sapphire

rm -rf vendor/xiaomi/miuicamera-sapphire
git clone -b 14 git@gitlab.com:kibria5/vendor_xiaomi_miuicamera-sapphire.git vendor/xiaomi/miuicamera-sapphire
```

5. Build rom!!!
6. Fix bug, include productivity and contribute to the overall project!!!

# Credits and thanks

- @kibria5
