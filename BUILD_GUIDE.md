# Build Guide

## Prerequisites

| Tool | Version |
|------|---------|
| **Qt** | 5.15+ (6.x works experimentally) |
| **CMake** | 3.20+ **or** `qmake` from Qt SDK |
| **GNU Make** | 4.0+ |
| **Sailfish SDK** | (for RPM generation) |

On Fedora‑like distros:

```bash
sudo dnf install qt5-qtbase-devel qt5-qtquickcontrols \
                 cmake gcc make sqlite-devel
```

## Build (Desktop)

```bash
git clone https://github.com/sorydima/GateWayChainForAuroraOS.git
cd GateWayChainForAuroraOS
mkdir build && cd build
cmake .. -DCMAKE_BUILD_TYPE=Release
make -j$(nproc)
./GateWayChain
```

## RPM Package (Aurora OS Device)

```bash
cd rpm
mb2 -t sailfish-armv7hl build
scp RPMS/*.rpm defaultuser@DEVICE:~
ssh defaultuser@DEVICE rpm -i gate-way-chain-*.rpm
```

_Last updated: 2025-07-06_
