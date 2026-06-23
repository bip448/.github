This organization centralizes work on the [BIP 448][bip-448] soft fork proposal.

BIP 448 emerged from the ongoing debate about making Bitcoin's scripting language more expressive. We argued in ["What's a good stopping point?"][stopping-point-post] that rebindable transactions, next-transaction commitment and signature verification for arbitrary messages are simple, well-understood capabilities that improve proven ways of scaling Bitcoin.
We later proposed a design for primitives enabling those capabilities in ["A Taproot-native (re-)bindable transactions bundle proposal"][bundle-proposal], drawing on previous attempts such as the [LNHANCE][lnhance] and [CTV+CSFS][ctv-csfs] proposals.

An implementation of BIP 448 is available for Bitcoin Inquisition: [#86](https://github.com/bitcoin-inquisition/bitcoin/pull/86) (`OP_INTERNALKEY`), [#87](https://github.com/bitcoin-inquisition/bitcoin/pull/87) (`OP_CHECKSIGFROMSTACK`), [#100](https://github.com/bitcoin-inquisition/bitcoin/pull/100) (`OP_TEMPLATEHASH`). The full bundle is pending Bitcoin Inquisition release to be usable on the Signet test network. \[TODO: link to a Bitcoin Core implementation as a PR in this organization?\]

#### Tooling

- BIP 448 integration in Miniscript / descriptors: [specifications][extension-tooling], Bitcoin Core implementation.
- BIP 448 integration in PSBTs: [specifications][extension-tooling], Bitcoin Core implementation.

#### Proof-of-concepts

- LN-symmetry with BIP 448: BOLT specifications, Core-Lightning implementation. \[TODO: PR both of those in this org and link them here\]
- 

[bip-448]: https://github.com/bitcoin/bips/blob/master/bip-0448.md
[stopping-point-post]: https://gnusha.org/pi/bitcoindev/F5vsDVNGXP_hmCvp4kFnptFLBCXOoRxWk9d05kSInq_kXj0ePqVAJGADkBFJxYIGkjk8Pw1gzBonTivH6WUUb4f6mwNCmJIwdXBMrjjQ0lI=@protonmail.com/
[bundle-proposal]: https://gnusha.org/pi/bitcoindev/26b96fb1-d916-474a-bd23-920becc3412cn@googlegroups.com/
[lnhance]: https://delvingbitcoin.org/t/lnhance-bips-and-implementation/376
[ctv-csfs]: https://gnusha.org/pi/bitcoindev/a86c2737-db79-4f54-9c1d-51beeb765163n@googlegroups.com/
[extension-tooling]: https://gnusha.org/pi/bitcoindev/9iwKoVRTokGsIwgHzGWO9ptfxAaIpJ_d8JY-uagbNnlKZK0WdUsl53IHO3kG2zcMmPObgDkHDltcVfZg7OAiZ5f11Tbt9e1vDW7GsOy-LeA=@protonmail.com/
