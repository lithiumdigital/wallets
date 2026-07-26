<!--
  GENERATED FILE -- do not edit by hand.
  Source of truth: wallets/*.yaml + wallets/_feature_registry.yaml
  Regenerate with: python3 scripts/generate_table.py
-->

# Wallet Directory

Source of truth for Canton Network wallet providers' supported features and
assets, per the Wallet Directory Program (see [CONTRIBUTING.md](./CONTRIBUTING.md)).

**Legend**

✅ self-attested -- click through to the evidence

🛡️ *name* verified by an independent third party -- click the name for their evidence

❌ *name* found this claim to be unsupported, contradicting the wallet -- click the name for their evidence

A linked "Not supported" means the wallet has said no with a reason

— no claim made either way.

## Wallet Overview & Primary Canton Network Features

| Feature | [Dfns](wallets/dfns.yaml) | [Send](wallets/send.yaml) | [Askardex Wallet](wallets/askardex-wallet.yaml) | [Cauri Wallet](wallets/cauri.yaml) | [Walley](wallets/walley.yaml) | [Blockdaemon Institutional Vault](wallets/blockdaemon-institutional-vault.yaml) | [Nightly](wallets/nightly.yaml) | [Metatarz](wallets/metatarz.yaml) | [Ledger Wallet](wallets/ledger-wallet.yaml) |
|---|---|---|---|---|---|---|---|---|---|
| **Wallet Overview** |  |  |  |  |  |  |  |  |  |
| &nbsp;&nbsp;&nbsp;&nbsp;Website | [https://www.dfns.co](https://www.dfns.co) | [https://cantonwallet.com](https://cantonwallet.com) | [https://wallet.askardex.com](https://wallet.askardex.com) | [https://cauri.cc](https://cauri.cc) | [https://walley.cc](https://walley.cc) | [https://www.blockdaemon.com/mpc-wallets-and-vaults/institutional-vault](https://www.blockdaemon.com/mpc-wallets-and-vaults/institutional-vault) | [https://nightly.app/wallet/canton](https://nightly.app/wallet/canton) | [https://wallet.metatarz.xyz](https://wallet.metatarz.xyz) | [https://www.ledger.com](https://www.ledger.com) |
| &nbsp;&nbsp;&nbsp;&nbsp;Added | 2026-07-24 | 2026-07-24 | 2026-07-25 | 2026-07-27 | 2026-07-27 | 2026-08-05 | 2026-08-11 | 2026-08-13 | 2026-08-17 |
| **Wallet Type** |  |  |  |  |  |  |  |  |  |
| &nbsp;&nbsp;&nbsp;&nbsp;Retail / Enterprise | Enterprise | Retail, Enterprise | Retail | retail | Retail | Enterprise | Retail | Retail, Enterprise | Retail |
| &nbsp;&nbsp;&nbsp;&nbsp;Custody Type | Self-custodial | Self-custodial | Self-custodial | self-custodial | Self-custodial | Self-custodial | Self-custodial | Self-custodial | Self-custodial |
| &nbsp;&nbsp;&nbsp;&nbsp;Form factor (Mobile / Browser / Desktop<br>/ Browser Extension / Hardware) | Browser | Browser, Mobile,<br>Browser-extension | Mobile | browser | Browser | Browser, Desktop, Mobile | Mobile, Browser-extension | Browser-extension | Hardware, Desktop, Mobile |
| &nbsp;&nbsp;&nbsp;&nbsp;Deployment Model (Self-hosted / SaaS /<br>Hybrid) | Self-hosted, SaaS, Hybrid | SaaS | SaaS | saas | SaaS | SaaS, Hybrid, On-prem | SaaS | Self-hosted, SaaS | Hybrid |
| **Canton Coin** |  |  |  |  |  |  |  |  |  |
| &nbsp;&nbsp;&nbsp;&nbsp;CC support | [✅](proofs/dfns/dfns-self-attestation.md#cc-support-cc_support) | ✅ | [✅](proofs/askardex-wallet/askardex-wallet-self-attestation.md#cc-support-cc_support) | [✅](proofs/cauri/cauri-self-attestation.md#cc-support-cc_support) | [✅](proofs/walley/walley-self-attestation.md#cc-support-cc_support) | [✅](proofs/blockdaemon-institutional-vault/blockdaemon-institutional-vault-self-attestation.md#cc-support-cc_support) | [✅](proofs/nightly/nightly-self-attestation.md#cc-support-cc_support) | [✅](proofs/metatarz/metatarz-self-attestation.md#cc-support-cc_support) | [✅](proofs/ledger-wallet/ledger-wallet-self-attestation.md#cc-support-cc_support) |
| &nbsp;&nbsp;&nbsp;&nbsp;Two-step CC transfers | — | — | — | [✅](proofs/cauri/cauri-self-attestation.md#two-step-cc-transfers-two_step_cc_transfers) | — | [✅](proofs/blockdaemon-institutional-vault/blockdaemon-institutional-vault-self-attestation.md#two-step-cc-transfers-two_step_cc_transfers) | [✅](proofs/nightly/nightly-self-attestation.md#two-step-cc-transfers-two_step_cc_transfers) | — | [✅](proofs/ledger-wallet/ledger-wallet-self-attestation.md#two-step-cc-transfers-two_step_cc_transfers) |
| &nbsp;&nbsp;&nbsp;&nbsp;Pre-approvals for CC | [✅](proofs/dfns/dfns-self-attestation.md#pre-approvals-for-cc-preapprovals) | ✅ | [✅](proofs/askardex-wallet/askardex-wallet-self-attestation.md#pre-approvals-for-cc-preapprovals) | [✅](proofs/cauri/cauri-self-attestation.md#pre-approvals-for-cc-preapprovals) | [✅](proofs/walley/walley-self-attestation.md#pre-approvals-for-cc-preapprovals) | [✅](proofs/blockdaemon-institutional-vault/blockdaemon-institutional-vault-self-attestation.md#pre-approvals-for-cc-preapprovals) | — | [✅](proofs/metatarz/metatarz-self-attestation.md#pre-approvals-for-cc-preapprovals) | [Not supported](wallets/ledger-wallet.yaml) |
| **Token Standard** |  |  |  |  |  |  |  |  |  |
| &nbsp;&nbsp;&nbsp;&nbsp;CIP-0056 token standard transfer support | [✅](proofs/dfns/dfns-self-attestation.md#cip-0056-token-standard-transfer-support-cip_0056_transfer) | ✅ | [✅](proofs/askardex-wallet/askardex-wallet-self-attestation.md#cip-0056-token-standard-transfer-support-cip_0056_transfer) | [✅](proofs/cauri/cauri-self-attestation.md#cip-0056-token-standard-transfer-support-cip_0056_transfer) | [✅](proofs/walley/walley-self-attestation.md#cip-0056-token-standard-transfer-support-cip_0056_transfer) | [✅](proofs/blockdaemon-institutional-vault/blockdaemon-institutional-vault-self-attestation.md#cip-0056-token-standard-transfer-support-cip_0056_transfer) | — | [✅](proofs/metatarz/metatarz-self-attestation.md#cip-0056-token-standard-transfer-support-cip_0056_transfer) | [✅](proofs/ledger-wallet/ledger-wallet-self-attestation.md#cip-0056-token-standard-transfer-support-cip_0056_transfer) |
| &nbsp;&nbsp;&nbsp;&nbsp;CIP-0056 token standard allocation support | — | ✅ | — | — | [✅](proofs/walley/walley-self-attestation.md#cip-0056-token-standard-allocation-support-cip_0056_allocation) | [✅](proofs/blockdaemon-institutional-vault/blockdaemon-institutional-vault-self-attestation.md#cip-0056-token-standard-allocation-support-cip_0056_allocation) | — | — | [Not supported](wallets/ledger-wallet.yaml) |
| &nbsp;&nbsp;&nbsp;&nbsp;CIP-112 token standard v2 support | — | ✅ | — | — | [Not supported](wallets/walley.yaml) | — | — | — | — |
| &nbsp;&nbsp;&nbsp;&nbsp;Memo tag support for transfers to omnibus accounts | [✅](proofs/dfns/dfns-self-attestation.md#memo-tag-support-for-transfers-to-omnibus-accounts-memo_tag_support) | ✅ | [✅](proofs/askardex-wallet/askardex-wallet-self-attestation.md#memo-tag-support-for-transfers-to-omnibus-accounts-memo_tag_support) | [✅](proofs/cauri/cauri-self-attestation.md#memo-tag-support-for-transfers-to-omnibus-accounts-memo_tag_support) | [✅](proofs/walley/walley-self-attestation.md#memo-tag-support-for-transfers-to-omnibus-accounts-memo_tag_support) | [✅](proofs/blockdaemon-institutional-vault/blockdaemon-institutional-vault-self-attestation.md#memo-tag-support-for-transfers-to-omnibus-accounts-memo_tag_support) | [✅](proofs/nightly/nightly-self-attestation.md#memo-tag-support-for-transfers-to-omnibus-accounts-memo_tag_support) | [✅](proofs/metatarz/metatarz-self-attestation.md#memo-tag-support-for-transfers-to-omnibus-accounts-memo_tag_support) | [✅](proofs/ledger-wallet/ledger-wallet-self-attestation.md#memo-tag-support-for-transfers-to-omnibus-accounts-memo_tag_support) |
| **dApp Connectivity (CIP-103)** |  |  |  |  |  |  |  |  |  |
| &nbsp;&nbsp;&nbsp;&nbsp;CIP-0103 dApp API support | — | ✅ | [✅](proofs/askardex-wallet/askardex-wallet-self-attestation.md#cip-0103-dapp-api-support-cip_0103_dapp_api) | [✅](proofs/cauri/cauri-self-attestation.md#cip-0103-dapp-api-support-cip_0103_dapp_api) | [✅](proofs/walley/walley-self-attestation.md#cip-0103-dapp-api-support-cip_0103_dapp_api) | — | [✅](proofs/nightly/nightly-self-attestation.md#cip-0103-dapp-api-support-cip_0103_dapp_api) | [✅](proofs/metatarz/metatarz-self-attestation.md#cip-0103-dapp-api-support-cip_0103_dapp_api) | [Not supported](wallets/ledger-wallet.yaml) |
| &nbsp;&nbsp;&nbsp;&nbsp;Wallet Connect support | [✅](proofs/dfns/dfns-self-attestation.md#wallet-connect-support-walletconnect_support) | ✅ | [✅](proofs/askardex-wallet/askardex-wallet-self-attestation.md#wallet-connect-support-walletconnect_support) | [✅](proofs/cauri/cauri-self-attestation.md#wallet-connect-support-walletconnect_support) | [Not supported](wallets/walley.yaml) | [✅](proofs/blockdaemon-institutional-vault/blockdaemon-institutional-vault-self-attestation.md#wallet-connect-support-walletconnect_support) | — | — | [Not supported](wallets/ledger-wallet.yaml) |

## Other Features

| Feature | [Dfns](wallets/dfns.yaml) | [Send](wallets/send.yaml) | [Askardex Wallet](wallets/askardex-wallet.yaml) | [Cauri Wallet](wallets/cauri.yaml) | [Walley](wallets/walley.yaml) | [Blockdaemon Institutional Vault](wallets/blockdaemon-institutional-vault.yaml) | [Nightly](wallets/nightly.yaml) | [Metatarz](wallets/metatarz.yaml) | [Ledger Wallet](wallets/ledger-wallet.yaml) |
|---|---|---|---|---|---|---|---|---|---|
| **App Specific** |  |  |  |  |  |  |  |  |  |
| &nbsp;&nbsp;&nbsp;&nbsp;Pre-approvals for DA Registry issued assets | [Not supported](wallets/dfns.yaml) | ✅ | — | [✅](proofs/cauri/cauri-self-attestation.md#pre-approvals-for-da-registry-issued-assets-registry_preapprovals) | [✅](proofs/walley/walley-self-attestation.md#pre-approvals-for-da-registry-issued-assets-registry_preapprovals) | — | — | [✅](proofs/metatarz/metatarz-self-attestation.md#pre-approvals-for-da-registry-issued-assets-registry_preapprovals) | — |
| &nbsp;&nbsp;&nbsp;&nbsp;Wallet Gateway signing driver | [✅](proofs/dfns/dfns-self-attestation.md#wallet-gateway-signing-driver-wallet_gateway_signing_driver) | — | — | — | [Not supported](wallets/walley.yaml) | [✅](proofs/blockdaemon-institutional-vault/blockdaemon-institutional-vault-self-attestation.md#wallet-gateway-signing-driver-wallet_gateway_signing_driver) | — | — | — |
| **Party Specific** |  |  |  |  |  |  |  |  |  |
| &nbsp;&nbsp;&nbsp;&nbsp;Key generation method | MPC/TSS -- keys generated as<br>distributed shares across<br>Dfns's signing network -- or<br>HSM-based key generation; no<br>seed phrases | Passkey-based (WebAuthn) key<br>generation on the user's<br>device; no seed phrases | Seed phrase (BIP-39 mnemonic,<br>24 words) | WebAuthn / passkey (Ed25519<br>via platform authenticator) | WebAuthn passkey PRF secret,<br>expanded with HKDF-SHA512 into<br>an Ed25519 signing key that is<br>generated and held in the<br>browser. A 24-word BIP-39<br>phrase backs up the same<br>secret. | MPC/TSS Distributed Key<br>Generation (Ed25519) | — | Seed phrase (BIP-39) | BIP-39 seed phrase; SLIP-10<br>Ed25519 keys derived and held<br>on the Ledger hardware device |
| &nbsp;&nbsp;&nbsp;&nbsp;Key recovery | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | — | ✅ | ✅ |
| &nbsp;&nbsp;&nbsp;&nbsp;Social recovery | — | — | — | — | [Not supported](wallets/walley.yaml) | — | — | — | — |
| &nbsp;&nbsp;&nbsp;&nbsp;Multi-address / account | ✅ | ✅ | — | — | [Not supported](wallets/walley.yaml) | ✅ | — | ✅ | ✅ |
| &nbsp;&nbsp;&nbsp;&nbsp;Distributed parties | — | ✅ | — | — | [Not supported](wallets/walley.yaml) | — | — | — | — |
| **Network Relevant Features** |  |  |  |  |  |  |  |  |  |
| &nbsp;&nbsp;&nbsp;&nbsp;UTXO merge delegation contract enabled | — | ✅ | — | [✅](proofs/cauri/cauri-self-attestation.md#utxo-merge-delegation-contract-enabled-utxo_merge_delegation) | [✅](proofs/walley/walley-self-attestation.md#utxo-merge-delegation-contract-enabled-utxo_merge_delegation) | — | — | — | — |
| **Validator Hosting** |  |  |  |  |  |  |  |  |  |
| &nbsp;&nbsp;&nbsp;&nbsp;Bring-Your-Own-Validator (BYOV) | ✅ | — | — | — | [Not supported](wallets/walley.yaml) | ✅ | — | — | — |
| &nbsp;&nbsp;&nbsp;&nbsp;Private validator | — | ✅ | — | — | — | ✅ | — | ✅ | — |
| &nbsp;&nbsp;&nbsp;&nbsp;Shared validator | — | ✅ | — | — | — | ✅ | — | — | — |
| **Transaction Signing** |  |  |  |  |  |  |  |  |  |
| &nbsp;&nbsp;&nbsp;&nbsp;Policy workflows | ✅ | ✅ | — | — | [Not supported](wallets/walley.yaml) | ✅ | — | — | — |
| &nbsp;&nbsp;&nbsp;&nbsp;Threshold Signature Scheme | ✅ | ✅ | — | — | [Not supported](wallets/walley.yaml) | ✅ | — | — | — |
| &nbsp;&nbsp;&nbsp;&nbsp;Hardware wallet support | [✅](proofs/dfns/dfns-self-attestation.md#hardware-wallet-support-hardware_wallet_support) | ✅ | — | — | [Not supported](wallets/walley.yaml) | — | — | — | [✅](proofs/ledger-wallet/ledger-wallet-self-attestation.md#hardware-wallet-support-hardware_wallet_support) |
| **Wallet Capabilities** |  |  |  |  |  |  |  |  |  |
| &nbsp;&nbsp;&nbsp;&nbsp;Compliance | SOC 2 Type II, ISO 27001, ISO<br>27017 and ISO 27018 certified;<br>built-in KYT/AML transaction<br>screening (Chainalysis,<br>Elliptic, Global Ledger) and<br>Travel Rule support (Notabene,<br>Sumsub, Global Ledger),<br>enforced through the policy<br>engine with audit logs | — | — | — | — | — | — | — | — |
| &nbsp;&nbsp;&nbsp;&nbsp;Tokenization | — | ✅ | — | — | — | [✅](proofs/blockdaemon-institutional-vault/blockdaemon-institutional-vault-self-attestation.md#tokenization-tokenization) | — | — | — |
| &nbsp;&nbsp;&nbsp;&nbsp;Reward minting | — | — | [✅](proofs/askardex-wallet/askardex-wallet-self-attestation.md#reward-minting-reward_minting) | — | [Not supported](wallets/walley.yaml) | [✅](proofs/blockdaemon-institutional-vault/blockdaemon-institutional-vault-self-attestation.md#reward-minting-reward_minting) | — | — | — |
| &nbsp;&nbsp;&nbsp;&nbsp;Transfer object / proof of transfer support | — | ✅ | — | — | [Not supported](wallets/walley.yaml) | — | — | — | — |
| &nbsp;&nbsp;&nbsp;&nbsp;Clear signing | [✅](proofs/dfns/dfns-self-attestation.md#clear-signing-clear_signing) | — | [✅](proofs/askardex-wallet/askardex-wallet-self-attestation.md#clear-signing-clear_signing) | [✅](proofs/cauri/cauri-self-attestation.md#clear-signing-clear_signing) | [✅](proofs/walley/walley-self-attestation.md#clear-signing-clear_signing) | [✅](proofs/blockdaemon-institutional-vault/blockdaemon-institutional-vault-self-attestation.md#clear-signing-clear_signing) | — | [✅](proofs/metatarz/metatarz-self-attestation.md#clear-signing-clear_signing) | [✅](proofs/ledger-wallet/ledger-wallet-self-attestation.md#clear-signing-clear_signing) |
| &nbsp;&nbsp;&nbsp;&nbsp;Integrated swaps | — | ✅ | [Not supported](wallets/askardex-wallet.yaml) | — | [✅](proofs/walley/walley-self-attestation.md#integrated-swaps-integrated_swaps) | — | — | — | — |
| &nbsp;&nbsp;&nbsp;&nbsp;Assets supported | CC, Other CIP-0056 tokens on<br>demand (token issuer provides<br>an RPC node) | CC, CIP-0056 tokens | CC, USDCx (CIP-0056), CBTC<br>(CIP-0056), CETH (CIP-0056),<br>HANDL (CIP-0056) | CC, USDCx, CBTC, HANDL,<br>cBondObl1, EDELx, cETH | CC, USDCx, CBTC, cETH, SBC,<br>raUSD, HANDL, EDELx, USDM1,<br>TRKX index tokens, Tradecraft<br>LP tokens, any CIP-0056 token<br>in the Walley registry (79<br>live at<br>api.walley.cc/v1/tokens) | CC, CIP-0056 utility tokens<br>(DA Utilities and DTCC<br>registry backends) | — | CC, USDC (CIP-0056), CBTC<br>(CIP-0056), CETH (CIP-0056),<br>HANDL (CIP-0056) | Canton Coin (CC), CIP-0056<br>token instruments |
| &nbsp;&nbsp;&nbsp;&nbsp;Languages supported | English | English | English | English | English | English | — | English | English, French, Spanish,<br>German, Japanese, Korean,<br>Portuguese (Brazil), Russian,<br>Turkish, Chinese (Simplified),<br>Thai |
