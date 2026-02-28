# Talero

Talero Network is a hybrid PoW/PoS EVM chain built for validators, stakers, and builders.

## Current Status

- Public repository initialized
- Distributable CPU miner package (Linux x86_64)
- GitHub release available for direct download
- SHA256 checksum published with release artifacts

## Release CPU Miner

Latest CPU miner release:

- https://github.com/TaleroDev/Talero/releases/latest

Artifacts:

- `talero-cpu-miner-linux-x86_64.zip`
- `talero-cpu-miner-linux-x86_64.zip.sha256`

## Quick Start (Miner)

```bash
unzip talero-cpu-miner-linux-x86_64.zip
cd talero-cpu-miner-linux-x86_64
sha256sum -c ../talero-cpu-miner-linux-x86_64.zip.sha256
cp .env.example .env
# edit .env (WALLET and WORKER)
./START.sh
```

## Notes

- The miner package contains runtime files only (binary, `.env` example, start script, guide).
- Source code is intentionally not included in the distributed archive.
