# Talero CPU Miner - Linux x86_64

Files:
- `talero-cpu-miner-linux-x86_64.zip`
- `talero-cpu-miner-linux-x86_64.zip.sha256`

Verification:
```bash
sha256sum -c talero-cpu-miner-linux-x86_64.zip.sha256
```

Install / run:
```bash
unzip talero-cpu-miner-linux-x86_64.zip
cd talero-cpu-miner-linux-x86_64
cp .env.example .env
# edit .env: WALLET + WORKER
./START.sh
```
