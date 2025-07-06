# Developer Guide

Welcome, hacker ♥

## Coding Style

* **C++17**, clang‑format (`.clang-format` in repo)  
* **QML** components in `LowerCamelCase.qml` files  
* UI strings go through `qsTr()` and are collected via `lupdate`

## Branch Flow

```
main ── stable releases
 |
 └─ feat/* , fix/* , doc/*  → squash‑merged via PR
```

## Commit Messages

```
type(scope): subject

body paragraph explaining *why*
```

`type` – choose among: feat, fix, perf, docs, test, build, ci, refactor, revert

## Tests

* Unit tests: `src/tests/` (QtTest)  
* CI runs on GitHub Actions (`.github/workflows/ci.yml`)

Run locally:

```bash
cmake -DBUILD_TESTING=ON ..
ctest --output-on-failure
```

## Localization

```bash
lupdate GateWayChain.pro
linguist translations/*.ts
lrelease translations/*.ts
```

_Last updated: 2025-07-06_
