# Cauri Wallet — Self-Attestation Evidence

Wallet name: `cauri`
Last updated: 2026-10-23

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

- Transaction update ID(s): `12205082...` (direct receive of 5.00 CC, 23 Oct 2026 11:50) — full ID via **View on Explorer** in the wallet
- Party ID(s): `cauri-sparrow::1220967b5c57730773375a12fef6982ef86142fe61ba94b00c4534f20a7f71ac810d`, counterparty `cauri-nectar::122028...087848`
- Explorer link(s): the party and its transfers are public on https://ccview.io — search `cauri-sparrow`
- Screenshot(s) / video:
  - ![activity](./cauri-self-attestation-images/cc_support-01-activity-sent-and-received.png) — activity list showing CC both sent and received
  - ![details](./cauri-self-attestation-images/cc_support-02-transaction-details-direct.png) — transaction detail with direction, counterparty, transaction ID and memo
- Notes: Performed on Canton MainNet. The wallet holds and transfers CC in both directions; the explorer records 45 updates and CC moving to and from this party.

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

- Transaction update ID(s) — step 1, offer created: on-ledger as an `AmuletTransferInstruction`; the wallet reports `OFFER CREATED; AWAITING RECIPIENT ACTION`
- Transaction update ID(s) — step 2, accepted and settled: `12207179...` (23 Oct 2026 11:42, type `OFFER`) — full ID via **View on Explorer**
- Party ID(s): sender `cauri-sparrow::1220967b5c57730773375a12fef6982ef86142fe61ba94b00c4534f20a7f71ac810d`, recipient `cauri-sparrow-2::1220514f1f60d7514b43a7193b0cc...c23c7e`
- Explorer link(s): https://ccview.io — search `cauri-sparrow`
- Screenshot(s) / video:
  - ![compose](./cauri-self-attestation-images/two_step_cc_transfers-01-compose-offer.png) — the wallet states `Direct transfer is unavailable for this recipient`, so the transfer becomes an offer
  - ![review](./cauri-self-attestation-images/two_step_cc_transfers-02-review-type-offer.png) — review shows `TYPE: OFFER` with an expiry
  - ![created](./cauri-self-attestation-images/two_step_cc_transfers-03-offer-created.png) — `OFFER CREATED; AWAITING RECIPIENT ACTION` — step 1 complete, not settled
  - ![pending](./cauri-self-attestation-images/two_step_cc_transfers-04-incoming-offer-pending.png) — the recipient sees an incoming offer awaiting Accept or Reject
  - ![accept](./cauri-self-attestation-images/two_step_cc_transfers-05-accept-dialog.png) — the recipient accepts — step 2
  - ![settled](./cauri-self-attestation-images/two_step_cc_transfers-06-settled-after-accept.png) — now `COMPLETED`, `+2.00 CC`, `TYPE: OFFER`
- Notes: Performed on Canton MainNet, 23 Oct 2026. 2 CC from `cauri-sparrow` to `cauri-sparrow-2`, which holds no CC pre-approval — so the transfer was created as an offer and settled only on the recipient's separate acceptance. Two distinct ledger transactions. Compare `preapprovals` below, where the same wallet sends to a pre-approved party and the transfer settles directly in one step.

---

## Pre-approvals for CC `preapprovals`

> Auto-accept incoming CC without manual confirmation. Distinct from
> registry_preapprovals (App Specific) below.
>
> Suggested test: Enable pre-approvals for CC. Send CC to the wallet address.
> Confirm the transfer was auto-accepted. Record the transaction update IDs
> and optionally provide screenshots of the holding, transfer, and party ID.

- Transaction update ID(s): `12205082...` (23 Oct 2026 11:50, type `DIRECT`) — full ID via **View on Explorer**
- Party ID(s): sender `cauri-sparrow::1220967b5c57730773375a12fef6982ef86142fe61ba94b00c4534f20a7f71ac810d`, recipient `cauri-nectar::122028...087848`
- Explorer link(s): https://ccview.io — search `cauri-sparrow`
- Screenshot(s) / video:
  - ![compose](./cauri-self-attestation-images/preapprovals-01-compose-no-offer-notice.png) — no offer notice, unlike the same screen for a party without a pre-approval
  - ![review](./cauri-self-attestation-images/preapprovals-02-review-type-direct.png) — review shows `TYPE: DIRECT`
  - ![confirmed](./cauri-self-attestation-images/preapprovals-03-confirmed-on-ledger.png) — `TYPE: DIRECT TRANSFER`, `Confirmed on ledger`, with no recipient action
- Notes: Performed on Canton MainNet, 23 Oct 2026. 5 CC to `cauri-nectar`, which holds a CC pre-approval; the transfer auto-settled with no acceptance step. The wallet decides direct against offer from the registry's transfer factory, so this is the same send flow taking the pre-approved path.

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

- Transaction update ID(s): `12205082...` (memo `CC to cauri-nectar`) and `12207179...` (memo `Some CC to cauri-sparrow-2`)
- Party ID(s): `cauri-sparrow::1220967b5c57730773375a12fef6982ef86142fe61ba94b00c4534f20a7f71ac810d`
- Explorer link(s): https://ccview.io — search `cauri-sparrow`
- Screenshot(s) / video:
  - ![compose](./cauri-self-attestation-images/two_step_cc_transfers-01-compose-offer.png) — the memo field on the send form
  - ![received](./cauri-self-attestation-images/cc_support-02-transaction-details-direct.png) — the memo preserved on the received transaction, readable by the recipient
- Notes: Performed on Canton MainNet, 23 Oct 2026. The memo travels with the transfer and is shown to the recipient on the settled transaction, which is what an exchange needs to credit a deposit. Carried on both the direct and the offer transfer above.

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
