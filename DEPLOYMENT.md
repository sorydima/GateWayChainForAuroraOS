# Deployment Guide

This document covers installing **GateWayChainForAuroraOS** on real devices and integrating it into a REChain swarm.

## 1. Obtain Matrix Credentials

Create an account on a REChain‑enabled homeserver (e.g. `matrix.rechain.network`). Note the *access token* and *device ID*.

## 2. Install the RPM

Follow *BUILD_GUIDE.md* or download the latest release RPM:

```bash
pkcon install-local gate-way-chain-<ver>.rpm
```

## 3. First‑Run Wizard

1. Launch *Gate Way* from the app grid  
2. Paste your Matrix homeserver URL and token  
3. Choose a **node name** (defaults to device hostname)  
4. The app will sync and begin participating in the mesh.

## 4. Autostart (optional)

Enable headless autostart:

```bash
systemctl --user enable --now gatewaychain
```

## 5. Updating

```bash
ssu ar rechain https://repos.rechain.network/aurora/latest
pkcon refresh
pkcon update gatewaychain
```

_Last updated: 2025-07-06_
