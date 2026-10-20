# Nostro Anchor API documentation

Mintlify project for the Stellar Anchor Platform / PI-SPI sandbox demonstration.

- `docs.json`: navigation and direct-browser API playground configuration.
- `openapi.json`: public SEP-10, SEP-12, SEP-31 and SEP-38 contract.
- `live-demo.mdx`: presenter walkthrough.
- `verified-demo.mdx`: recorded Testnet and virtual-money evidence.

Connect this repository's `main` branch to Mintlify, with documentation root `/`.

This repository contains public documentation only. It does not contain the backend implementation, wallet keys, API credentials, customer database or bearer tokens. The canonical contract and runtime live separately in the Nostro backend's isolated `feature/stellar-anchor-demo` branch under `anchor-demo/`.

To update the contract, synchronize `anchor-demo/docs/openapi.json` from its canonical source, then copy the documentation files here and push a reviewed commit. If the temporary sandbox origin changes, update both runtime discovery and this OpenAPI server URL before presenting.

## Published demonstration (20 October 2026)

Live site: https://nostro.mintlify.site

The hosted Mintlify editor is the publishing source for now. GitHub synchronization is **not connected**: its OAuth flow requested broader access than the approved documentation-only repository. This repository contains the full source package; the hosted site currently publishes the overview, a condensed payment walkthrough at `/quickstart`, and all OpenAPI operations. Changes pushed here are not automatically published.

A payout was created using the published Mintlify playground and funded by the local signer:

- SEP-31 transaction: `ee234c5f-81d2-425c-adbf-abba50beaa6e`
- Stellar Testnet hash: `bc45466ce35b3114bcf800a8d612c5c43bbcb9a6b7125b352364d74269e0fa94`
- PI-SPI reference: `ESNB99920261020092253eKGT8Z5QwgnWm8`
- Result: `completed`, 0.2 Testnet USDC → 100 virtual XOF, 2026-10-20T09:22:57.136380Z.

The public docs remain hosted; live API requests depend on the operator's local services and ngrok tunnel. Authentication tokens expire. Wallet signing remains local.
