# Zachary Alexander

I'm setting up [Nonceworks](https://nonceworks.com): hosted OpenZeppelin Monitor (1.6.0) and Relayer (1.8.0) for small teams that lost Defender on 2026-07-01. The images are the upstream ones, pinned by digest, and the relayer signs with a key in the team's own AWS KMS, Google Cloud KMS or Turnkey account, so I never hold key material.

Work in the open:

- [defender-action2plugin](https://github.com/zachsplat/defender-action2plugin): scaffold a Relayer plugin from a retired Defender Action.
- [relayer-808-repro](https://github.com/zachsplat/relayer-808-repro): OpenZeppelin Relayer issue #808 (a transaction that reaches gas_price_cap is never resent), reproduced on 1.8.0.
- [relayer-817-repro](https://github.com/zachsplat/relayer-817-repro) and [relayer-843-repro](https://github.com/zachsplat/relayer-843-repro): a mined transaction finalized as Failed on a stale receipt, and a nonce-too-high jam that never heals, both reproduced on 1.8.0.
- [openzeppelin-relayer #912](https://github.com/OpenZeppelin/openzeppelin-relayer/issues/912): the relayer's EVM policies do not cover its sign endpoints.
- [Upgrading the Relayer from 1.4 to 1.8](https://nonceworks.com/notes/relayer-1-4-to-1-8-upgrade-notes.html).
- Notes on Monitor and Relayer bugs, with the error strings to search for: https://nonceworks.com/notes.html

Secret values for a Nonceworks stack are sent encrypted with [age](https://age-encryption.org) to this key, the same one published at https://nonceworks.com/age.txt:

```
age1engh35zk5tsch46n0q2uz09q0q38wr8ks099wehpljnjc7t953zspkjk3h
```

Not affiliated with OpenZeppelin. Nonceworks is one person, with no SLA and no audit. If your relayer or monitor broke in July, write to me on [Telegram](https://t.me/zachary_alexander_dev) or at zachary_dev@icloud.com.
