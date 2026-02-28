# Talero

Talero Network est une chaine EVM hybride PoW/PoS conçue pour les validateurs, stakers et builders.

## Etat actuel

- Dépôt public initialisé
- Package CPU miner distribuable (Linux x86_64)
- Release GitHub disponible en téléchargement direct
- Checksum SHA256 publié avec les artefacts

## Release CPU Miner

Dernière release CPU miner:

- https://github.com/TaleroDev/Talero/releases/latest

Artefacts:

- `talero-cpu-miner-linux-x86_64.zip`
- `talero-cpu-miner-linux-x86_64.zip.sha256`

## Démarrage rapide (Miner)

```bash
unzip talero-cpu-miner-linux-x86_64.zip
cd talero-cpu-miner-linux-x86_64
sha256sum -c ../talero-cpu-miner-linux-x86_64.zip.sha256
cp .env.example .env
# éditer .env (WALLET et WORKER)
./START.sh
```

## Notes

- Le package miner contient uniquement les fichiers runtime (binaire, exemple `.env`, script de lancement, guide).
- Le code source n'est volontairement pas embarqué dans l'archive distribuée.
