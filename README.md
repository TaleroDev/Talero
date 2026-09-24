# Talero

Talero Network is a hybrid PoW/PoS EVM chain built for validators, stakers,
miners, and builders.

## Talero CPU Miner v0.7.0

The official CPU miner release is available from the
[GitHub Releases page](https://github.com/TaleroDev/Talero/releases/tag/v0.7.0).

The release provides a statically linked 64-bit Linux binary, configuration
templates, checksums, and complete deployment instructions. No source code,
credentials, wallet data, or runtime state is included in the archive.

### Download and verify

Download both release assets:

- `talero-cpu-miner-v0.7.0-linux-x86_64-musl-static-source-8a44bf5c6ce5-20260924-091747.zip`
- `talero-cpu-miner-v0.7.0-linux-x86_64-musl-static-source-8a44bf5c6ce5-20260924-091747.zip.sha256`

Verify the archive before extracting it:

```bash
sha256sum -c talero-cpu-miner-v0.7.0-linux-x86_64-musl-static-source-8a44bf5c6ce5-20260924-091747.zip.sha256
unzip talero-cpu-miner-v0.7.0-linux-x86_64-musl-static-source-8a44bf5c6ce5-20260924-091747.zip
cd talero-cpu-miner-v0.7.0-linux-x86_64-musl-static-source-8a44bf5c6ce5-20260924-091747
sha256sum -c SHA256SUMS
```

Every checksum must report `OK`. The expected SHA-256 digest of the ZIP is:

```text
b15a8e53259cae0caede150e58b2bb73f48e858e02006b575d11f2ca24e6703b
```

### Configure the miner

Read `README.md` and `docs/CREATE_MINING_KEY.md` inside the extracted archive.
Create the mining credentials on a trusted computer and transfer only the
mining key and delegation file to the mining rig. Never copy the payment-wallet
private key to the rig.

Create the runtime configuration:

```bash
cp .env.example .env
chmod 600 .env
```

Replace every placeholder in `.env`. The required settings include:

```dotenv
STRATUM_HOST=stratum+tls://pool.talero.info:3333
STRATUM_POOL_AUDIENCE=pool.talero.info
STRATUM_CHAIN_TAG=talero-mainnet
WALLET=tlro:0xYOUR_PAYMENT_ADDRESS
WORKER=YOUR_UNIQUE_WORKER_NAME
MINING_PRIVATE_KEY_FILE=/var/lib/talero-cpu-miner/mining.key
MINING_DELEGATION_FILE=/var/lib/talero-cpu-miner/mining-delegation.json
MINER_STATE_DIR=/var/lib/talero-cpu-miner
```

Do not place private keys directly in `.env`.

### Start the miner

```bash
./talero-cpu-miner --version
./start.sh
```

Confirm that the miner connects, authorizes the worker, receives work, and
reports accepted shares. Optional CPU presets are provided in `profiles/`.

### Run as a service

The deployment guide inside the archive includes a complete systemd service
example, update procedure, credential rotation guidance, and removal steps.

## Disclaimer

Review [DISCLAIMER.md](DISCLAIMER.md) before using Talero software or
participating in the network.
