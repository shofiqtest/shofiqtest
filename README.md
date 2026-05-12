# Md Shofiqul Islam

**Linux Kernel Contributor · SoC Software Engineer · C/C++ · Telco & Embedded Systems**

Espoo, Finland &nbsp;|&nbsp; [linkedin.com/in/mdshofiqul](https://linkedin.com/in/mdshofiqul) &nbsp;|&nbsp; [lore.kernel.org](https://lore.kernel.org/all/?q=Md+Shofiqul+Islam) &nbsp;|&nbsp; shofiqtest@gmail.com

---

## About

SoC Software Engineer with 5+ years building performance-critical C/C++ software for 5G beamforming platforms on Linux at Nokia. Active upstream Linux kernel contributor with **10 patches** across **7 subsystems** — 6 merged into mainline, 4 awaiting maintainer pickup. Deep expertise in real-time embedded Linux, latency-sensitive data plane engineering, and kernel-level performance tuning.

Currently open to new opportunities in Linux systems, Telco, and embedded software engineering across Europe.

---

## Linux Kernel Contributions

All patches visible at [lore.kernel.org/all/?q=Md+Shofiqul+Islam](https://lore.kernel.org/all/?q=Md+Shofiqul+Islam)

| Patch | Subsystem | Status |
|---|---|---|
| `iio: adc: ti-ads1298` — Remove incorrect test signal init (functional bug fix) | IIO | ✅ Applied — Jonathan Cameron · iio/togreg |
| `iio: adc: ti-ads1298` — Fix incorrect timeout comment | IIO | ✅ Merged — mainline |
| `iio: accel: adxl345/313/367/380` — Add timestamp to FIFO data | IIO | ✅ Merged — mainline |
| `ASoC: nau8825` — Fix typos in comments | ASoC | ✅ Merged — broonie/sound.git |
| `net/sctp` — Fix typo in comment | SCTP | ✅ Merged — netdev/net-next · applied by Jakub Kicinski · [`c7ea0d2b4d76`](https://git.kernel.org/netdev/net-next/c/c7ea0d2b4d76) |
| `xfs` — Fix typo in comment | XFS | ✅ Accepted — Carlos Maiolino · [`509fdeb3326b`](https://git.kernel.org/pub/scm/linux/kernel/git/djwong/xfs-linux.git) |
| `scsi: scsi_scan` — Fix spelling in comment | SCSI | 🔄 Reviewed-by Bart Van Assche · awaiting maintainer |
| `scsi: storvsc` — Replace symbolic permissions with octal | SCSI | 🔄 Reviewed-by Long Li (Microsoft) · awaiting maintainer |
| `power: supply` — Fix typos in comments | Power | 🔄 Acked-by Linus Walleij · awaiting maintainer |
| `soc: ti: knav_qmss_queue` — Implement resource cleanup in remove() | SoC / TI | 🔄 v2 submitted · Suggested-by Nishanth Menon (TI) |

---

## Projects

### [High-Performance Event Processing Engine (C++)](https://github.com/shofiqtest/high-performance-event-engine)
Lock-free MPMC ring buffer built with C++17 atomics. Cache-line aligned, zero-copy hot path, `std::variant` dispatch.

- **8–12M events/sec** at **1–5 µs** latency (4 producers / 4 consumers)
- **15–20M events/sec** at **2–8 µs** latency (8 producers / 8 consumers)
- Dmitry Vyukov bounded queue algorithm · CAS operations · false-sharing elimination

`C++17` `std::atomic` `Lock-Free` `CMake` `Cache-Line Alignment`

---

### [Zephyr RTOS: MAX30102 Sensor Driver](https://github.com/zephyrproject-rtos/zephyr/pull/108697)
Upstream I2C optical heart-rate sensor driver for the Zephyr sensor subsystem. Full Kconfig integration, DTS binding, and CI build verification (498/498 steps).

`C` `Zephyr RTOS` `I2C` `Sensor Subsystem` `DeviceTree`

---

## Skills

```
Languages:   C · C++ · Python · Bash · ARM Assembly
Kernel:      Linux kernel upstream · device drivers · IIO · SCSI · XFS · Power · SoC/TI · networking stack
Telco / 5G:  Nokia 5G SoC · RF/L1 · NFV · O-RAN · real-time data plane
Performance: CPU pinning · NUMA affinity · perf · ftrace · ASan/TSan · lock-free structures
Build:       Yocto/BitBake · CMake · Git · Gerrit · Jenkins
Containers:  Docker · Podman · Linux namespaces/cgroups (kernel level)
```

---

## Background

- **Nokia** — SoC Software Engineer, Espoo (2023–2026) · RF/L1 Software Engineer, Oulu (2022–2023)
- **Etteplan** — Software Test & Automation Engineer, Tampere (2021–2022)
- M.Sc. Biomedical Engineering — University of Oulu, Finland
- M.Sc. Computer Science & Engineering — Islamic University, Bangladesh
