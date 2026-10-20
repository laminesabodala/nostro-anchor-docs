# Nostro Anchor API documentation

Mintlify sources for the Stellar Anchor Platform / PI-SPI sandbox demonstration.

- Live walkthrough: https://nostro.mintlify.site/quickstart
- Hosted API: https://sandbox-api.nostro.finance
- Runtime, tests, canonical contract and OVH deployment: https://github.com/laminesabodala/nostro-anchor-demo
- `docs.json`: navigation and API playground configuration.
- `openapi.json`: public SEP-10, SEP-12, SEP-31 and SEP-38 contract, plus sandbox helpers.
- `quickstart.mdx`: browser-only payment walkthrough.
- `test-beneficiaries.mdx`: supported bank and mobile-money fixtures.
- Other guides and screenshots retain earlier demonstration evidence.

The hosted Mintlify editor is the publishing source. GitHub synchronization is not connected: its OAuth flow requested broader access than the approved documentation-only repository. Pushing here saves source changes but does not automatically publish them. Import the updated OpenAPI and changed pages into the hosted editor, review, and publish.

This repository contains documentation only. Credentials, signing keys, bearer tokens and database backups must not be committed. The canonical OpenAPI source is `contracts/public-openapi.json` in the runtime repository; synchronize its `docs/` copy and this repository when changing the API.

## Verified OVH deployment — 20 October 2026

The demo runs on OVH independently of the development computer. Both flows were completed through the published Mintlify playground, including server-sponsored Stellar Testnet funding and PI-SPI sandbox payouts:

| Route | Amount | SEP-31 payment ID | Result |
| --- | --- | --- | --- |
| Bank | 1.4 USDC → 700 XOF | `3eea415e-fa9a-4169-88b9-3e50910d66d2` | completed |
| Mobile money | 0.6 USDC → 300 XOF | `a9c4e85c-5129-460f-875b-dff223a5eb11` | completed |

[Bank funding on Testnet](https://stellar.expert/explorer/testnet/tx/a65f8c1c57b3952b2af000504b17b21197760414b767cdecde54022189bc9db4) · [Mobile-wallet funding on Testnet](https://stellar.expert/explorer/testnet/tx/0918d1ebf0e30093b326ebc3d2272ba194f4330b5b4148ac3c74bb8f78d2cf74)

A full server reboot preserved transactions. Both database backups were restored in isolation and verified. See the runtime repository's `deploy/README.md` for operations and recovery limitations. All funds and destinations here are test environments; a blockchain funding transaction alone is not evidence of the off-chain payout.
