The [BIP 448][bip-448] soft fork proposal emerged from the ongoing debate about making Bitcoin's scripting language more expressive.

In ["What's a good stopping point?"][stopping-point-post], we argued that rebindable transactions, next-transaction commitment and signature verification for arbitrary messages are simple, well-understood capabilities that improve proven ways of scaling Bitcoin.

In ["A Taproot-native (re-)bindable transactions bundle proposal"][bundle-proposal], we subsequently proposed a design for a set of primitives providing these capabilities, drawing on previous attempts such as the [LNHANCE][lnhance] and [CTV+CSFS][ctv-csfs] proposals.

This organization centralizes the work on demonstrating the use cases for this bundle of primitives.

### Implementation

- Bitcoin Inquisition: [#86](https://github.com/bitcoin-inquisition/bitcoin/pull/86) (`OP_INTERNALKEY`), [#87](https://github.com/bitcoin-inquisition/bitcoin/pull/87) (`OP_CHECKSIGFROMSTACK`), [#100](https://github.com/bitcoin-inquisition/bitcoin/pull/100) (`OP_TEMPLATEHASH`).
- Bitcoin Core master: [full BIP 448 implementation (no activation)](https://github.com/bip448/bitcoin/pull/1).

The full bundle will be usable on the main Signet test network with the upcoming release of Bitcoin Inquisition.

### Tooling

- BIP 448 integration in Miniscript / descriptors: [specifications][extension-tooling], Bitcoin Core implementation ([WIP](https://github.com/bitcoin-inquisition/bitcoin/pull/108)).
- BIP 448 integration in PSBTs: [specifications][extension-tooling], Bitcoin Core implementation ([WIP](https://github.com/bitcoin-inquisition/bitcoin/pull/108)).
- Various Rust-Bitcoin tooling: rust-bitcoin integration ([master](https://github.com/bip448/rust-bitcoin/pull/1), [0.32.x](https://github.com/bip448/rust-bitcoin/pull/2)), *TODO: more*.

### Proof-of-concepts

- Close last pinning vector in Lightning: https://github.com/bip448/bolts/pull/2.
- LN-symmetry with BIP 448: [BOLT specifications](https://github.com/bip448/bolts/pull/1), [Core-Lightning implementation](https://github.com/bip448/lightning/pull/1).
- Ark with `OP_TEMPLATEHASH`: *TODO*.
- Erk detailed specifications: *TODO*.

[bip-448]: https://github.com/bitcoin/bips/blob/master/bip-0448.md
[stopping-point-post]: https://gnusha.org/pi/bitcoindev/F5vsDVNGXP_hmCvp4kFnptFLBCXOoRxWk9d05kSInq_kXj0ePqVAJGADkBFJxYIGkjk8Pw1gzBonTivH6WUUb4f6mwNCmJIwdXBMrjjQ0lI=@protonmail.com/
[bundle-proposal]: https://gnusha.org/pi/bitcoindev/26b96fb1-d916-474a-bd23-920becc3412cn@googlegroups.com/
[lnhance]: https://delvingbitcoin.org/t/lnhance-bips-and-implementation/376
[ctv-csfs]: https://gnusha.org/pi/bitcoindev/a86c2737-db79-4f54-9c1d-51beeb765163n@googlegroups.com/
[extension-tooling]: https://gnusha.org/pi/bitcoindev/9iwKoVRTokGsIwgHzGWO9ptfxAaIpJ_d8JY-uagbNnlKZK0WdUsl53IHO3kG2zcMmPObgDkHDltcVfZg7OAiZ5f11Tbt9e1vDW7GsOy-LeA=@protonmail.com/
