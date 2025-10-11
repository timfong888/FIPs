# Automatic FIP Archival System

This repository includes an automatic archival system that saves approved FIPs to permanent decentralized storage on Filecoin.

## How It Works

When someone comments **"FIP approved"** on any issue, the system automatically:

1. Extracts complete FIP data (issue, comments, linked PRs, code changes)
2. Creates a self-contained HTML archive with clickable links
3. Uploads to Filecoin with cryptographic proof (PDP)
4. Comments back with IPFS gateway URLs and verification links

## Viewing Archived FIPs

Archives can be accessed via IPFS gateways with all links working:
- `https://ipfs.io/ipfs/[ROOT_CID]/index.html`
- `https://dweb.link/ipfs/[ROOT_CID]/index.html`

All internal links (PRs, diffs, comments) work seamlessly when viewed via IPFS gateways.

## Setup & Usage

See [QUICKSTART.md](QUICKSTART.md) for setup instructions.
See [TESTING.md](TESTING.md) for testing guide.

## Manual Archival

You can also manually archive any FIP:

\`\`\`bash
node scripts/archive-fip.js --issue 123
\`\`\`

## Features

- **Permanent Storage** - FIPs stored on the Filecoin network
- **Cryptographic Proof** - PDP verifies ongoing data possession
- **IPFS Gateway Compatible** - All links work via ipfs.io and dweb.link
- **Self-Contained** - Complete history with no external dependencies
- **Public Verification** - Anyone can verify archives on blockchain

## Repository

Built with [filecoin-pin](https://github.com/filecoin-project/filecoin-pin)
