# Zachary Alexander

I run [Nonceworks](https://nonceworks.com/pricing.html?src=gh). Nonceworks checks crypto teams' release, publish and nightly workflows every week, against the next GitHub runner image and the next version of each base image, and sends the fix as a pull request when one is about to break or has quietly stopped shipping. It also hosts OpenZeppelin Monitor and Relayer with the signing key in the team's own KMS.

## Recent merged fixes

All of them, with what broke and when: [nonceworks.com/fixes.html](https://nonceworks.com/fixes.html?src=gh).

- [tangle-network/blueprint#1621](https://github.com/tangle-network/blueprint/pull/1621): the x86_64 Linux release build moved to Ubuntu 24.04, ahead of Ubuntu 26.04's GCC 15, which does not compile the RocksDB 8.1.1 headers in its dependency tree.
- [MystenLabs/deepbookv3#1426](https://github.com/MystenLabs/deepbookv3/pull/1426): the test-indexer job moved to Ubuntu 24.04 before GCC 15 and PostgreSQL 18 on 26.04 reached it.
- [cosmos/chain-registry#8107](https://github.com/cosmos/chain-registry/pull/8107): the IBC data tests moved from Python 3.9, which setup-python does not build for Ubuntu 26.04, to 3.12.
- [cowprotocol/bff#279](https://github.com/cowprotocol/bff/pull/279): node:lts moved to Node 26, whose images ship without yarn; a maintainer merged the Dockerfile change from my [#278](https://github.com/cowprotocol/bff/pull/278) as part of this pull request.
- [superfluid-org/protocol-monorepo#2252](https://github.com/superfluid-org/protocol-monorepo/pull/2252): the new default reward addresses in the published metadata, cherry-picked by a maintainer from my [#2244](https://github.com/superfluid-org/protocol-monorepo/pull/2244) and released as metadata 1.6.6.

## A report on your organisation

Send your organisation's GitHub name to hello@nonceworks.com and Nonceworks will send back a report on its public release, publish and nightly workflows: what is already failing, what shipped without its assets, and what breaks on the next runner. For public repositories it is free. The [pricing page](https://nonceworks.com/pricing.html?src=gh) covers private repositories and the weekly watch.

## Tools

- [upgrade-canary](https://github.com/zachsplat/upgrade-canary): catches container images that build green and then do not start, and previews floating base tag moves (node:lts, ubuntu:latest, python:3) before they land. CLI and GitHub Action.
- [relayer-failure-lab](https://github.com/zachsplat/relayer-failure-lab): release tests for OpenZeppelin Relayer, four open issues reproduced on each release, plus a config validator CLI and GitHub Action.
- [relayer-843-repro](https://github.com/zachsplat/relayer-843-repro), [relayer-817-repro](https://github.com/zachsplat/relayer-817-repro) and [relayer-808-repro](https://github.com/zachsplat/relayer-808-repro): a nonce-too-high jam that never heals, a mined transaction finalized as Failed on a stale receipt, and a transaction at gas_price_cap that is never resent, each reproduced on Relayer 1.8.0.
- [defender-action2plugin](https://github.com/zachsplat/defender-action2plugin): scaffold a Relayer plugin from a retired Defender Action.
- [openzeppelin-relayer #912](https://github.com/OpenZeppelin/openzeppelin-relayer/issues/912): the relayer's EVM policies do not cover its sign endpoints.

Secret values for a hosted Nonceworks stack are sent encrypted with [age](https://age-encryption.org) to this key, the same one published at https://nonceworks.com/age.txt:

```
age1engh35zk5tsch46n0q2uz09q0q38wr8ks099wehpljnjc7t953zspkjk3h
```

Not affiliated with OpenZeppelin. No SLA, and no audit of Nonceworks itself. Write to hello@nonceworks.com or on [Telegram](https://t.me/zachary_alexander_dev).
