# Talero CPU Miner - Linux x86_64

Fichiers:
- `talero-cpu-miner-linux-x86_64.zip`
- `talero-cpu-miner-linux-x86_64.zip.sha256`

Verification:
```bash
sha256sum -c talero-cpu-miner-linux-x86_64.zip.sha256
```

Installation / lancement:
```bash
unzip talero-cpu-miner-linux-x86_64.zip
cd talero-cpu-miner-linux-x86_64
cp .env.example .env
# éditer .env: WALLET + WORKER
./START.sh
```
