# Talero CPU Miner - Linux x86_64

Fichiers:
- `talero-cpu-miner-linux-x86_64.tar.gz`
- `talero-cpu-miner-linux-x86_64.tar.gz.sha256`

Verification:
```bash
sha256sum -c talero-cpu-miner-linux-x86_64.tar.gz.sha256
```

Installation / lancement:
```bash
tar -xzf talero-cpu-miner-linux-x86_64.tar.gz
cd talero-cpu-miner-linux-x86_64
cp .env.example .env
# edit .env: WALLET + WORKER
./start_miner.sh
```
