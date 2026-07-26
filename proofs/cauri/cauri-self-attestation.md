# Cauri Wallet — Self-Attestation Evidence

Wallet name: `cauri`
Last updated: 2026-07-27

<!--
Structure-only draft. Each heading below is present so the wallet YAML's
`proof:` anchors resolve during review. Evidence (update IDs, party IDs,
explorer links, screenshots) is filled in via a follow-up commit before this
PR is opened upstream. See CONTRIBUTING.md.
-->

---

## CC support `cc_support`

> Send, receive, and hold Canton Coin.
>
> Suggested test: Send CC to and from the wallet. Record the transaction
> update IDs and optionally provide screenshots of the holding, transfer, and
> party ID.

- Transaction update ID(s): _TBD — pending evidence commit_
- Party ID(s): _TBD_
- Explorer link(s): _TBD_
- Screenshot(s) / video: _TBD_
- Notes: _TBD_

---

## Two-step CC transfers `two_step_cc_transfers`

> Send CC as an offer the receiver accepts, rather than a single atomic send.
> Cauri picks the form from the registry's transfer factory: a receiver with a
> CC pre-approval settles directly, and one without gets a two-step offer.
>
> Suggested test: Perform a two-step CC transfer (propose/create followed by a
> separate accept/settle step, rather than a single atomic send). Record the
> transaction update ID(s) for both steps and optionally provide screenshots of
> each.

- Transaction update ID(s) — step 1, AmuletTransferInstruction created: _TBD — pending evidence commit_
- Transaction update ID(s) — step 2, TransferInstruction_Accept: _TBD_
- Party ID(s): _TBD_
- Explorer link(s): _TBD_
- Screenshot(s) / video: _TBD_
- Notes: _TBD_

---

## Pre-approvals for CC `preapprovals`

> Auto-accept incoming CC without manual confirmation. Distinct from
> registry_preapprovals (App Specific) below.
>
> Suggested test: Enable pre-approvals for CC. Send CC to the wallet address.
> Confirm the transfer was auto-accepted. Record the transaction update IDs
> and optionally provide screenshots of the holding, transfer, and party ID.

- Transaction update ID(s): _TBD — pending evidence commit_
- Party ID(s): _TBD_
- Explorer link(s): _TBD_
- Screenshot(s) / video: _TBD_
- Notes: _TBD_

---

## CIP-0056 token standard transfer support `cip_0056_transfer`

> Send and receive any CIP-0056 token, not just CC.
>
> Suggested test: Send a CIP-0056-compatible token (not Canton Coin) to and
> from the wallet. Record the transaction update IDs and optionally provide
> screenshots of the holding, transfer, and party ID.

- Transaction update ID(s): _TBD — pending evidence commit_
- Party ID(s): _TBD_
- Explorer link(s): _TBD_
- Screenshot(s) / video: _TBD_
- Notes: _TBD_

---

## CIP-0103 dApp API support `cip_0103_dapp_api`

> Connect to and sign transactions from a third-party dApp via CIP-0103.
>
> Suggested test: Connect to a dApp using a CIP-0103 connection. Initiate a
> transaction from within the dApp and sign it from the wallet. Confirm the
> successful transaction. Optionally provide screenshots or a video
> recording.

- Transaction update ID(s): _TBD — pending evidence commit_
- Party ID(s): _TBD_
- Explorer link(s): _TBD_
- Screenshot(s) / video: _TBD_
- Notes: _TBD_

---

## Wallet Connect support `walletconnect_support`

> Connect to and sign transactions from a third-party dApp via Wallet
> Connect.
>
> Suggested test: Connect to a dApp using Wallet Connect. Initiate a
> transaction from within the dApp and sign it from the wallet. Confirm the
> successful transaction. Optionally provide screenshots or a video
> recording.

- Transaction update ID(s): _TBD — pending evidence commit_
- Party ID(s): _TBD_
- Explorer link(s): _TBD_
- Screenshot(s) / video: _TBD_
- Notes: _TBD_

---

## Memo tag support for transfers to omnibus accounts `memo_tag_support`

> Attach a memo tag to a transfer, recorded under the
> splice.lfdecentralizedtrust.org/reason metadata.
>
> Suggested test: Include a memo tag in an asset transfer (this can be
> combined with the cc_support test). Record the transaction update ID
> showing the memo tag under the splice.lfdecentralizedtrust.org/reason
> metadata in the transaction JSON.

- Transaction update ID(s): _TBD — pending evidence commit_
- Party ID(s): _TBD_
- Explorer link(s): _TBD_
- Screenshot(s) / video: _TBD_
- Notes: _TBD_

---

## Pre-approvals for DA Registry issued assets `registry_preapprovals`

> Auto-accept incoming registry-issued (non-CC) assets. Distinct from
> preapprovals (Canton Coin) above.
>
> Suggested test: Register pre-approvals for a DA Registry issued asset.
> Send the asset to the wallet address. Confirm the asset was auto-accepted.
> Record the transaction update IDs and optionally provide screenshots of
> the holding, transfer, and party ID.

- Transaction update ID(s): _TBD — pending evidence commit_
- Party ID(s): _TBD_
- Explorer link(s): _TBD_
- Screenshot(s) / video: _TBD_
- Notes: _TBD_

---

## UTXO merge delegation contract enabled `utxo_merge_delegation`

> The wallet enables the merge delegation contract so UTXOs can be
> consolidated on-chain, reducing UTXO bloat.
>
> Suggested test: Enable the merge delegation contract in the wallet.
> Witness a UTXO consolidation contract on-chain for CC (sender & receiver
> are the same party).

- Transaction update ID(s): _TBD — pending evidence commit_
- Party ID(s): _TBD_
- Explorer link(s): _TBD_
- Screenshot(s) / video: _TBD_
- Notes: _TBD_

---

## Clear signing `clear_signing`

> The wallet displays human-readable transaction details (not raw
> hex/opaque data) before signing.
>
> Suggested test: Show the wallet displaying human-readable transaction
> details (not raw hex/opaque data) before signing. Provide a screenshot of
> the clear-signing confirmation screen for a real transaction, alongside
> its transaction update ID.

- Transaction update ID(s): _TBD — pending evidence commit_
- Party ID(s): _TBD_
- Explorer link(s): _TBD_
- Screenshot(s) / video: _TBD_
- Notes: _TBD_
