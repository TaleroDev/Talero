# Talero

Talero Network is a hybrid PoW/PoS EVM chain built for validators, stakers, and builders.

## What Is Already Implemented

- Public repository initialized
- CPU miner distributable package (Linux x86_64)
- GitHub Release for direct download
- SHA256 checksum published with the release asset

## CPU Miner Release

Latest CPU miner release:

- https://github.com/TaleroDev/Talero/releases/tag/v0.1.0-cpu-miner-linux-x86_64

Assets:

- `talero-cpu-miner-linux-x86_64.tar.gz`
- `talero-cpu-miner-linux-x86_64.tar.gz.sha256`

## Quick Start (Miner)

```bash
tar -xzf talero-cpu-miner-linux-x86_64.tar.gz
cd talero-cpu-miner-linux-x86_64
sha256sum -c talero-cpu-miner-linux-x86_64.tar.gz.sha256
cp .env.example .env
# edit .env (WALLET and WORKER)
./start_miner.sh
```

## Notes

- The miner package contains runtime files only (binary, env example, launcher script, install guide).
- Source code is intentionally not bundled in the distributable archive.
