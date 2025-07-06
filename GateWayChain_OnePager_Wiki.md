# GateWayChain for Aurora OS

GateWayChain is a native Qt/QML app for **Aurora OS (Sailfish fork)** that acts as a REChain node interface.  
It integrates with Matrix via `libQuotient` for decentralized message transport and supports embedded SQLite for local state.  
The app is designed to run smoothly on mobile devices with minimal resources.

## ✨ Features

- Native AuroraOS (QML) interface
- Encrypted Matrix client for REChain gossip layer
- SQLite state persistence
- RPM packaging for ARM devices
- Full support for offline-first node participation
- Built-in developer diagnostics (console, logs, tracing)

## 📁 Repo Structure

| Folder          | Purpose |
|-----------------|---------|
| `src/`          | C++ logic & core REChain integration |
| `qml/`          | QML UI components |
| `translations/` | Localized `.ts` files |
| `rpm/`          | Sailfish/AuroraOS RPM packaging |
| `scripts/`      | Build & release helpers |
| `.github/`      | CI workflow for build & test |

## 🛠️ Build Quickstart

```bash
git clone https://github.com/sorydima/GateWayChainForAuroraOS.git
cd GateWayChainForAuroraOS
mkdir build && cd build
cmake .. -DCMAKE_BUILD_TYPE=Release
make -j$(nproc)
./GateWayChain
```

For RPM builds, use `mb2` inside Sailfish SDK (see `BUILD_GUIDE.md`).

## 🧑‍💻 Dev Tips

- Follow `DEVELOPER_GUIDE.md` for style, tests, and commit structure
- CI/CD pipeline defined in `.github/workflows/ci.yml`
- Run unit tests with `ctest`
- Localize using `lupdate`, `linguist`, and `lrelease`

## 📦 Release Flow

1. Merge all PRs to `main`
2. Bump version in `.pro` and `spec`
3. Tag with `vX.Y.Z`, run release script
4. Upload RPM/AppImage/Flatpak to GitHub

See `RELEASE.md` for details.

## 📚 Docs

- `BUILD_GUIDE.md` — compilation & install
- `DEPLOYMENT.md` — on-device setup
- `GOVERNANCE.md` — decision-making
- `ARCHITECTURE.md` — system layout
- `DEVELOPER_GUIDE.md` — contributing tips

---
Maintained by [@sorydima](https://github.com/sorydima) · Last updated: 2025-07-06