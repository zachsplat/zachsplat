### zachary alexander

embedded linux and systems engineer. C, C++, OCaml, Go, Python. daily linux user.

I work on embedded linux devices, IoT deployments, and systems software. interested in the whole stack from bootloader to userspace -- secure boot, device trees, kernel tuning, distribution packaging, and keeping things running reliably in the field.

also into distributed systems, storage engines, and networking internals when I get the chance.

#### embedded linux / IoT

- [snap-builder](https://github.com/zachsplat/snap-builder) - snap packaging helpers for Ubuntu Core, cross-compilation for ARM64/ARMhf
- [efi-boot-shim](https://github.com/zachsplat/efi-boot-shim) - UEFI secure boot chain tools, key management, MOK enrollment
- [rt-linux-bench](https://github.com/zachsplat/rt-linux-bench) - PREEMPT_RT latency benchmarking, CPU isolation, IRQ tuning
- [device-tree-tools](https://github.com/zachsplat/device-tree-tools) - DT overlay utilities for hardware bring-up (I2C, SPI, CAN)
- [ota-updater](https://github.com/zachsplat/ota-updater) - A/B partition OTA firmware updates with rollback
- [initramfs-builder](https://github.com/zachsplat/initramfs-builder) - custom initramfs for embedded devices, dm-verity support
- [mqtt-gateway](https://github.com/zachsplat/mqtt-gateway) - MQTT gateway bridging modbus/serial sensors to cloud
- [sysdiag](https://github.com/zachsplat/sysdiag) - system diagnostics toolkit for field debugging

#### systems / networking

- [ocaml-kv](https://github.com/zachsplat/ocaml-kv) - embedded kv store with TCP interface in OCaml
- [raft-ocaml](https://github.com/zachsplat/raft-ocaml) - raft consensus, leader election + log replication
- [lsm-engine](https://github.com/zachsplat/lsm-engine) - LSM tree storage engine in C++
- [pcap-tool](https://github.com/zachsplat/pcap-tool) - pcap parser with TCP flow tracking
- [memalloc](https://github.com/zachsplat/memalloc) - pool/slab allocator in C
- [dns-resolver](https://github.com/zachsplat/dns-resolver) - recursive DNS resolver in Go
- [tcp-proxy](https://github.com/zachsplat/tcp-proxy) - reverse proxy with connection pooling
