<div align="center">

# Md Shofiqul Islam

**Embedded Linux BSP Engineer · Yocto/U-Boot · Linux Kernel Contributor · Zephyr Individual Contributor · IEC 62304 Medical**

**11 patches merged to Linus Torvalds mainline Linux kernel**

<a href="mailto:shofiqtest@gmail.com"><img alt="Email" src="https://img.shields.io/badge/Email-shofiqtest%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white"></a>
<a href="https://www.linkedin.com/in/mdshofiqul/"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-Md%20Shofiqul%20Islam-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"></a>
<a href="https://lore.kernel.org/all/?q=Md+Shofiqul+Islam"><img alt="Kernel patches" src="https://img.shields.io/badge/Kernel%20Patches-lore.kernel.org-F8C517?style=for-the-badge&logo=linux&logoColor=black"></a>
<a href="https://kernel-medical.github.io/linux-medical-bsp/"><img alt="Medical BSP Service" src="https://img.shields.io/badge/IEC%2062304%20BSP%20Service-linux--medical--bsp-2ea043?style=for-the-badge&logo=linux&logoColor=white"></a>

📍 Espoo, Finland · Open to embedded Linux / medical device roles in Europe and remote

![Profile views](https://komarev.com/ghpvc/?username=shofiqtest&color=2ea043&style=flat&label=Profile+views)

</div>

---

## What I Do

| Area | Detail |
|---|---|
| **Yocto BSP** | Owner of ARM SoC BSP layer for production ARM SoC platform — machine config, BitBake recipes, kernel LTS upgrades, CI/CD pipeline |
| **Linux kernel drivers** | **11 patches merged to mainline** (Torvalds tree) across 9 subsystems — IIO, MFD, power, SoC, SCSI, xfs, sctp, ASoC, DRM/Accel |
| **U-Boot** | NXP i.MX6Q patches — SPL SRAM overflow fix, LDB clock swap fix, VPD reader fix |
| **Zephyr RTOS** | Individual Contributor — MAX30102 SpO₂/HR sensor driver merged, Arm TSC reviewed |
| **Medical device** | IEC 62304 + ISO 14971 — Class IIb CE-marked device firmware, M.HSc. Biomedical Engineering |

---

## Yocto / BSP / U-Boot

### Yocto / OpenEmbedded (daily work)

I **own the Yocto BSP layer** for a production ARM SoC platform:
- Machine configuration, kernel recipes, BitBake layer hierarchy
- Cross-compilation toolchain and sysroot management
- Kernel LTS version upgrades — API migration, Device Tree updates, hardware regression validation
- CI/CD pipeline: automated build, boot, and regression testing across board variants

### U-Boot (NXP i.MX6Q)

Patches for NXP i.MX6Q LDB display clock initialisation and common board code.

| Patch | Files | Status |
|---|---|---|
| [`ge: common: vpd_reader: fix errloc array size in verify_bch()`](https://lore.kernel.org/u-boot/20260630133939.1472106-1-shofiqtest@gmail.com/) | `board/ge/common/vpd_reader.c` | 🔄 Reviewed — Ian Ray |
| [`clk: imx6q: guard LDB clock init with appropriate video config`](https://lore.kernel.org/u-boot/20260630120417.1469554-2-shofiqtest@gmail.com/) | `drivers/clk/imx/clk-imx6q.c`, `board/aristainetos/aristainetos.c` | 🔄 Under review |
| [`imx6: clock: fix clk0/clk1 swap in select_ldb_di_clock_source()`](https://lore.kernel.org/u-boot/20260630120417.1469554-3-shofiqtest@gmail.com/) | `arch/arm/mach-imx/mx6/clock.c` | 🔄 Under review |

**Root cause found during review:** `clk0`/`clk1` were written to `LDB_DI1`/`LDB_DI0` respectively — reversed. Guard mismatch: function defined for `CONFIG_SPL_VIDEO` but called for `!CONFIG_SPL_BUILD`. SPL SRAM overflow of 112 bytes. Fixed with `!CONFIG_SPL_BUILD || CONFIG_SPL_VIDEO` — saved 688 bytes in SPL.

---

## IEC 62304 Compliance Documents for Embedded OSS Drivers

IEC 62304-aligned documentation based on real upstream drivers — real code, real documentation discipline.

**MAX30102** (Zephyr RTOS, [merged PR #108697](https://github.com/zephyrproject-rtos/zephyr/pull/108697)):

| Document | Standard | Description |
|---|---|---|
| [Software Requirements Specification](https://github.com/shofiqtest/iec62304-embedded-drivers/blob/main/SRS_MAX30102_Driver.md) | IEC 62304 §5.2 | 12 shall-statements: functional, performance, interface and safety requirements |
| [Software Design Specification](https://github.com/shofiqtest/iec62304-embedded-drivers/blob/main/SDS_MAX30102_Driver.md) | IEC 62304 §5.4 | Architecture, component design, interfaces, timing, concurrency |
| [SOUP Record](https://github.com/shofiqtest/iec62304-embedded-drivers/blob/main/SOUP_Record_MAX30102_Driver.md) | IEC 62304 §8 | SOUP management for Zephyr RTOS dependencies with risk classification |
| [FMEA](https://github.com/shofiqtest/iec62304-embedded-drivers/blob/main/FMEA_MAX30102_Driver.md) | ISO 14971:2019 | 8 failure modes — severity, probability, risk level, mitigations |

**ADS1299** (Linux kernel IIO, [patch submitted](https://lore.kernel.org/linux-iio/20260630140311.1473031-2-shofiqtest@gmail.com/)):

| Document | Standard | Description |
|---|---|---|
| [SOUP Record](https://github.com/shofiqtest/iec62304-embedded-drivers/blob/main/SOUP_Record_ADS1299_Driver.md) | IEC 62304 §8 | SOUP identification, known anomalies, risk classification, verification |
| [FMEA](https://github.com/shofiqtest/iec62304-embedded-drivers/blob/main/FMEA_ADS1299_Driver.md) | ISO 14971:2019 | 10 failure modes for 24-bit EEG acquisition — signal integrity, lead-off, SPI errors |

Documents: [iec62304-embedded-drivers](https://github.com/shofiqtest/iec62304-embedded-drivers) · Tool: [kernel-soup-gen](https://github.com/kernel-medical/kernel-soup-gen) — auto-generate SOUP records for any Linux kernel driver

---

## Zephyr RTOS Contributions

| Contribution | Area | Status |
|---|---|---|
| [`drivers: sensor: max3010x: MAX30102 SpO₂ and heart-rate driver`](https://github.com/zephyrproject-rtos/zephyr/pull/108697) | I2C, interrupt-driven FIFO, Devicetree binding, Kconfig, build coverage | ✅ **Merged** — Arm TSC reviewed · [PR #108697](https://github.com/zephyrproject-rtos/zephyr/pull/108697) |
| `maxim,max3010x-common` shared DT binding | Pulse oximeter / heart-rate sensor family | ✅ **Merged** |
| `tests/drivers/build_all/sensor/i2c.dtsi` coverage | Zephyr sensor build test matrix | ✅ **Merged** |

Recognised as **Zephyr Individual Contributor**.

---

## Linux Kernel Contributions

**11 patches merged to [Linus Torvalds mainline](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/log/?qt=author&q=Shofiqul) · 6 more under review**

Full history: [lore.kernel.org](https://lore.kernel.org/all/?q=Md+Shofiqul+Islam)

### Merged to mainline ✅

| Patch | Subsystem | Merged |
|---|---|---|
| [`iio: adc: ti-ads1298: Remove unnecessary CONFIG2 write during init`](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=01437ab5111f57005be54005f5b575dc06cb682e) | IIO / Medical ADC | 2026-05-31 |
| [`iio: adc: ti-ads1298: Fix incorrect timeout comment`](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=d0f23d8a9091f43329e79bcd29bcac6bf81205e5) | IIO / Medical ADC | 2026-05-31 |
| [`iio: adc: ti-ads1298: Add parentheses around macro parameter`](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=5d7b3df5c1be8f46c2d3eabd1c1fd7b27294cbd3) | IIO / Medical ADC | 2026-05-31 |
| [`mfd: si476x-i2c: Fix spelling mistakes in comments`](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=a44ec8fd3839434c0c85ae68106a94081a31341f) | MFD | 2026-06-17 |
| [`power: supply: ab8500_fg: Fix typos in comments`](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=15384402c94a55b05d06a446aedd19e242367b6f) | Power Supply | 2026-06-03 |
| [`soc: ti: knav_qmss_queue: Implement resource cleanup in remove()`](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=10a1969353b20caa50c320717e054601631c0d3e) | SoC / TI Keystone | 2026-05-15 |
| [`scsi: storvsc: Replace symbolic permissions with octal`](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=73322071418ec3ad5e4d9cdf783890d7f2ae9777) | SCSI / Hyper-V | 2026-05-14 |
| [`scsi: core: scsi_scan: Fix typo in comment`](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=036218473a8467493860df84602a7825b71385af) | SCSI core | 2026-05-14 |
| [`xfs: Fix typo in comment`](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=509fdeb3326be0db055e88d0f689a3888f147f90) | XFS Filesystem | 2026-05-11 |
| [`sctp: Fix typo in comment`](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=c7ea0d2b4d76bf70bd5f108fa07506640b78ce05) | Networking / SCTP | 2026-05-08 |
| [`ASoC: nau8825: Fix typos in comments`](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=5f1752afb464a82bdc372281ed7313aa4663b269) | Sound / ASoC | 2026-05-06 |

### Under review 🔄

| Patch | Subsystem | Status |
|---|---|---|
| [`iio: adc: ti-ads1298: add ADS1299 EEG ADC family support`](https://lore.kernel.org/linux-iio/20260630140311.1473031-2-shofiqtest@gmail.com/) | IIO / Medical ADC / EEG | v2 in progress |
| [`dt-bindings: iio: adc: ti,ads1298: add ADS1299 EEG ADC variants`](https://lore.kernel.org/linux-iio/20260630140311.1473031-1-shofiqtest@gmail.com/) | DT Bindings / IIO | v2 in progress |
| [`iio: health: add MAX86150 ECG and PPG biosensor driver`](https://lore.kernel.org/linux-iio/20260623140113.12574-1-shofiqtest@gmail.com/) | IIO / Health / Biosensor | v3 in progress |
| [`dt-bindings: iio: accel: Convert lis302 binding to YAML schema`](https://lore.kernel.org/linux-iio/20260609214753.4479-1-shofiqtest@gmail.com/) | DT Bindings / IIO | Under review |
| [`drm/accel/amdxdna: add debugfs support`](https://lore.kernel.org/dri-devel/20260519203236.252068-1-shofiqtest@gmail.com/) | DRM Accel / AMD Ryzen AI NPU | Under review |
| [`drm/accel/ivpu: send exact IPC message size instead of union size`](https://lore.kernel.org/dri-devel/177922807295.254725.11654057638908709302@gmail.com/) | DRM Accel / Intel VPU NPU | Under review |

---

## Networking & Data Center Open Source

### DPDK (Data Plane Development Kit)

| Patch | Component | Status |
|---|---|---|
| [`bus/fslmc: fix ignored return value in fslmc_bus_unplug`](https://inbox.dpdk.org/dev/20260513203725.1905-2-shofiqtest@gmail.com/) | NXP DPAA2 bus driver | ✅ Merged — Hemant Agrawal (NXP), David Marchand (Red Hat) |
| [`dma/dpaa2: fix dpaa2_qdma_remove always returning success`](https://inbox.dpdk.org/dev/20260513203725.1905-3-shofiqtest@gmail.com/) | NXP DPAA2 DMA driver | ✅ Merged |

### SONiC (Software for Open Networking in the Cloud)

| Patch | Component | Status |
|---|---|---|
| [`pfcwd: fix TypeError crash in interval() on partial PFC_WD entries`](https://github.com/sonic-net/sonic-utilities/pull/4541) | PFC Watchdog CLI | 🔄 Open — DCO ✅ · EasyCLA ✅ |

---

## Education

- **M.HSc. Biomedical Engineering** — [University of Oulu](https://www.oulu.fi/en/), Finland (2016–2021)
- **M.Sc. Computer Science & Engineering** — [Islamic University, Kushtia](https://www.iu.ac.bd/), Bangladesh (2014–2015)
- **B.Sc. Electrical & Electronics Engineering** — [International Islamic University Chittagong](https://www.iiuc.ac.bd/), Bangladesh (2008–2013)

## Certifications

Linux for Engineers — The Linux Foundation · Introduction to RISC-V (LFD110) — The Linux Foundation · Generative AI and LLMs — Coursera

---

## Tools

<p>
<img alt="Linux Kernel" src="https://img.shields.io/badge/Linux_Kernel-FCC624?style=flat-square&logo=linux&logoColor=black">
<img alt="Yocto" src="https://img.shields.io/badge/Yocto-BSP_owner-6E9A4B?style=flat-square">
<img alt="U-Boot" src="https://img.shields.io/badge/U--Boot-contributor-003087?style=flat-square">
<img alt="C" src="https://img.shields.io/badge/C-expert-00599C?style=flat-square&logo=c&logoColor=white">
<img alt="C++" src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=c%2B%2B&logoColor=white">
<img alt="Zephyr" src="https://img.shields.io/badge/Zephyr_RTOS-Individual_Contributor-0F172A?style=flat-square">
<img alt="Python" src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white">
<img alt="git" src="https://img.shields.io/badge/git_send--email-active-orange?style=flat-square">
<img alt="IEC62304" src="https://img.shields.io/badge/IEC_62304-medical_device-red?style=flat-square">
<img alt="Docker" src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white">
<img alt="checkpatch" src="https://img.shields.io/badge/checkpatch-passing-brightgreen?style=flat-square">
</p>
