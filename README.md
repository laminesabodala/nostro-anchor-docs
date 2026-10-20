# Nostro Anchor API documentation

Mintlify project for the Stellar Anchor Platform / PI-SPI sandbox demonstration.

- `docs.json`: navigation and direct-browser API playground configuration.
- `openapi.json`: public SEP-10, SEP-12, SEP-31 and SEP-38 contract.
- `live-demo.mdx`: presenter walkthrough.
- `verified-demo.mdx`: recorded Testnet and virtual-money evidence.

Connect this repository's `main` branch to Mintlify, with documentation root `/`.

This repository contains public documentation only. It does not contain the backend implementation, wallet keys, API credentials, customer database or bearer tokens. The canonical contract and runtime live separately in the Nostro backend's isolated `feature/stellar-anchor-demo` branch under `anchor-demo/`.

To update the contract, synchronize `anchor-demo/docs/openapi.json` from its canonical source, then copy the documentation files here and push a reviewed commit. If the temporary sandbox origin changes, update both runtime discovery and this OpenAPI server URL before presenting.
