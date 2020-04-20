# OrangeFOX Recovery Device configuration for R11s

Copyright 2019 - The OmniROM Project

For building OrangeFOX Recovery for oppo r11s.

### OrangeFOX Source
OrangeFOX: https://gitlab.com/OrangeFox/Manifest

### How to build recovery

###-----First,Sync source

mkdir OrangeFox

cd OrangeFox

repo init --depth=1 -u https://gitlab.com/OrangeFox/Manifest.git -b fox_9.0

repo sync -j8 --force-sync

mkdir -p device/oppo

cd device/oppo

git clone https://github.com/loserq/OrangeFox_device_oppo_r11s.git 

###-----Next,Build Recovery

cd OrangeFox

source build/envsetup.sh

export ALLOW_MISSING_DEPENDENCIES=true

export LC_ALL="C"

lunch omni_r11s-eng && mka recoveryimage

### Device specifications
=====================================

Basic   | Spec Sheet
-------:|:-------------------------
CPU     | Kryo (2.2+1.8GHz)
CHIPSET | Qualcomm sdm660 
GPU     | Adreno 512
Memory  | 4GB
Shipped Android Version | 9.0 (Pie)
Storage | 64GB
Battery | 3205 mAh
Dimensions | 155.8 x 76 x 6.1 mm
Display | 2160x1080 pixels/5" LCD
Rear Camera  | 20+16 MP
Front Camera | 20 MP

# OrangrFox_device_oppo_r11s
