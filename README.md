<div align="center">

# Md Shofiqul Islam

**Embedded Linux BSP Engineer · Nokia SoC · Yocto/U-Boot · Linux Kernel Driver Contributor · Zephyr Individual Contributor · IEC 62304 Medical**

<a href="mailto:shofiqtest@gmail.com"><img alt="Email" src="https://img.shields.io/badge/Email-shofiqtest%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white"></a>
<a href="https://www.linkedin.com/in/mdshofiqul/"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-Md%20Shofiqul%20Islam-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"></a>
<a href="https://lore.kernel.org/all/?q=Md+Shofiqul+Islam"><img alt="Kernel patches" src="https://img.shields.io/badge/Kernel%20Patches-lore.kernel.org-F8C517?style=for-the-badge&logo=linux&logoColor=black"></a>

📍 Espoo, Finland · Open to embedded Linux / medical device roles in Europe and remote

</div>

---

## What I Do

| Area | Detail |
|---|---|
| **Yocto BSP** | Owner of Nokia's ARM SoC BSP layer — machine config, BitBake recipes, kernel LTS upgrades, CI/CD pipeline |
| **Linux kernel drivers** | 15 upstream patches across 9 subsystems — IIO, DMA, DT bindings, networking, SCSI, DRM/Accel |
| **U-Boot** | NXP i.MX6Q patches — SPL SRAM overflow fix, LDB clock swap fix, board/ge/b1x5v2/ board file |
| **Zephyr RTOS** | Individual Contributor — MAX30102 SpO₂/HR sensor driver merged, Arm TSC reviewed |
| **Medical device** | IEC 62304 + ISO 14971 — Class IIb CE-marked device at Sooma Medical, M.HSc. Biomedical Engineering |

---

## Yocto / BSP / U-Boot

### Yocto / OpenEmbedded (Nokia — daily work)

At Nokia I **own the Yocto BSP layer** for an ARM SoC platform:
- Machine configuration, kernel recipes, BitBake layer hierarchy
- Cross-compilation toolchain and sysroot management
- Kernel LTS version upgrades — API migration, Device Tree updates, hardware regression validation
- CI/CD pipeline: automated build, boot, and regression testing across board variants

| Patch | Layer | Status |
|---|---|---|
| [`libusb1: upgrade 1.0.29 → 1.0.30`](https://lists.openembedded.org/g/openembedded-core) | `openembedded-core` · `meta/recipes-support/libusb` | 🔄 Submitted |

### U-Boot (NXP i.MX6Q — ge_b1x5v2 board)

Three patches fixing LDB display clock initialization on NXP i.MX6Q. Patch 3 directly modifies `board/ge/b1x5v2/b1x5v2.c` and `board/aristainetos/aristainetos.c`.

| Patch | Files | Status |
|---|---|---|
| [SPL SRAM overflow fix — guard `of_assigned_ldb_sels()` with `!CONFIG_SPL_BUILD`](https://lore.kernel.org/all/CAOMZO5De=9ECdSZ=VxvhrAJxRX7vpHu65hCueUn7VChmBnYPxQ@mail.gmail.com/) | `drivers/clk/imx/clk-imx6q.c` | ✅ Sent |
| [`imx6: clock: fix clk0/clk1 swap in select_ldb_di_clock_source()`](https://lore.kernel.org/u-boot/20260518215445.175753-2-shofiqtest@gmail.com/) | `arch/arm/mach-imx/mx6/clock.c` | 🔄 Under review |
| [`imx6: guard LDB clock init with appropriate video config`](https://lore.kernel.org/u-boot/20260518215445.175753-3-shofiqtest@gmail.com/) | `drivers/clk/imx/clk-imx6q.c`, `board/ge/b1x5v2/b1x5v2.c`, `board/aristainetos/aristainetos.c` | 🔄 Under review |

**Root cause found during review:** `clk0`/`clk1` were written to `LDB_DI1`/`LDB_DI0` respectively — reversed. Guard mismatch: function defined for `CONFIG_SPL_VIDEO` but called for `!CONFIG_SPL_BUILD`. SPL SRAM overflow of 112 bytes. Fixed with `!CONFIG_SPL_BUILD || CONFIG_SPL_VIDEO` — saved 688 bytes in SPL.

---

## Medical Device Software Portfolio

IEC 62304-aligned artefacts based on the MAX30102 Zephyr RTOS driver (merged upstream, [PR #108697](https://github.com/zephyrproject-rtos/zephyr/pull/108697)) — real driver, real documentation discipline.

| Document | Standard | Description |
|---|---|---|
| [Software Requirements Specification](https://github.com/shofiqtest/embedded-medical-software-portfolio/blob/main/SRS_MAX30101_Driver.md) | IEC 62304 §5.2 | 12 shall-statements: functional, performance, interface and safety requirements |
| [Software Design Specification](https://github.com/shofiqtest/embedded-medical-software-portfolio/blob/main/SDS_MAX30101_Driver.md) | IEC 62304 §5.4 | Architecture, component design, interfaces, timing, concurrency |
| [SOUP Record](https://github.com/shofiqtest/embedded-medical-software-portfolio/blob/main/SOUP_Record_MAX30101_Driver.md) | IEC 62304 §8 | SOUP management for Zephyr RTOS dependencies with risk classification |
| [FMEA](https://github.com/shofiqtest/embedded-medical-software-portfolio/blob/main/FMEA_MAX30101_Driver.md) | ISO 14971:2019 | 8 failure modes — severity, probability, risk level, mitigations |

Sooma Medical experience: Class IIb CE-marked device, full design history file, ISO 14971 hazard analysis, requirements-to-verification traceability matrix.

Repository: [embedded-medical-software-portfolio](https://github.com/shofiqtest/embedded-medical-software-portfolio)

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

15 patches across 9 subsystems. Full history: [lore.kernel.org](https://lore.kernel.org/all/?q=Md+Shofiqul+Islam)

| Patch | Subsystem | Status |
|---|---|---|
| [`iio: health: add MAX86150 ECG and PPG biosensor driver`](https://lore.kernel.org/linux-iio/20260623140113.12574-1-shofiqtest@gmail.com/) | IIO / Health / Biosensor | 🔄 Under review |
| [`iio: adc: ti-ads1298: Remove unnecessary CONFIG2 write during init`](https://www.spinics.net/lists/kernel/msg6192186.html) | IIO / Medical ADC | ✅ In linux-next |
| [`iio: adc: ti-ads1298: Fix incorrect timeout comment`](https://lore.kernel.org/linux-iio/?q=ti-ads1298+timeout+shofiqtest) | IIO / Medical ADC | ✅ In linux-next |
| [`iio: adc: ti-ads1298: Add parentheses around macro parameter`](https://www.spinics.net/lists/kernel/msg6191377.html) | IIO / Medical ADC | ✅ In linux-next |
| [`dt-bindings: iio: accel: Convert lis302 binding to YAML schema`](https://lore.kernel.org/linux-iio/20260609214753.4479-1-shofiqtest@gmail.com/) | DT Bindings / IIO | 🔄 Under review |
| [`sctp: Fix typo in comment`](https://git.kernel.org/netdev/net-next/c/c7ea0d2b4d76) | Networking / SCTP | ✅ Merged — Jakub Kicinski |
| [`ASoC: nau8825: Fix typos in comments`](https://git.kernel.org/broonie/sound/c/5f1752afb464) | Sound / ASoC | ✅ Merged |
| [`xfs: Fix typo in comment`](https://www.spinics.net/lists/kernel/msg6190059.html) | XFS Filesystem | ✅ Accepted |
| [`scsi: scsi_scan: Fix typo in comment`](https://lore.kernel.org/linux-scsi/20260506094504.25381-1-shofiqtest@gmail.com/) | SCSI core | ✅ Merged — Martin K. Petersen |
| [`scsi: storvsc: Replace symbolic permissions with octal`](https://lore.kernel.org/linux-scsi/20260506004948.18017-1-shofiqtest@gmail.com/) | SCSI / Hyper-V | ✅ Merged — reviewed by Microsoft |
| [`power: supply: ab8500_fg: Fix typos in comments`](https://www.spinics.net/lists/kernel/msg6189221.html) | Power Supply | ✅ In linux-next |
| [`soc: ti: knav_qmss_queue: Implement resource cleanup in remove()`](https://www.spinics.net/lists/kernel/msg6189942.html) | SoC / TI Keystone | ✅ Applied — Nishanth Menon |
| [`mfd: si476x-i2c: Fix spelling mistakes in comments`](https://lore.kernel.org/linux-mfd/20260514181954.1442-1-shofiqtest@gmail.com/) | MFD / Si476x | ✅ In linux-next |
| [`drm/accel/amdxdna: add debugfs support`](https://lore.kernel.org/dri-devel/20260519203236.252068-1-shofiqtest@gmail.com/) | DRM Accel / AMD Ryzen AI NPU | 🔄 Under review |
| [`drm/accel/ivpu: send exact IPC message size instead of union size`](https://lore.kernel.org/dri-devel/177922807295.254725.11654057638908709302@gmail.com/) | DRM Accel / Intel VPU NPU | 🔄 Under review |

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
<img alt="Git" src="https://img.shields.io/badge/git_send--email-active-orange?style=flat-square">
<img alt="IEC62304" src="https://img.shields.io/badge/IEC_62304-medical_device-red?style=flat-square">
<img alt="Docker" src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white">
<img alt="checkpatch" src="https://img.shields.io/badge/checkpatch-passing-brightgreen?style=flat-square">
</p>
