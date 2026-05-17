<div align="center">

# Hi there, I'm Shofiq

**Linux Kernel Contributor** - **U-Boot Contributor** - **Zephyr RTOS Contributor (merged)** - **Quantum Computing Contributor** - **SONiC Contributor** - **DPDK Contributor** - **SoC Software Engineer**  
**C/C++** - **Embedded Linux** - **Systems & Runtime** - **Docker** - **Kubernetes**

<a href="mailto:shofiqtest@gmail.com"><img alt="Email" src="https://img.shields.io/badge/Email-shofiqtest%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white"></a>
<a href="https://www.linkedin.com/in/mdshofiqul/"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-Md%20Shofiqul%20Islam-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"></a>
<a href="https://lore.kernel.org/all/?q=Md+Shofiqul+Islam"><img alt="Kernel patches" src="https://img.shields.io/badge/Kernel%20Patches-lore.kernel.org-F8C517?style=for-the-badge&logo=linux&logoColor=black"></a>
<a href="https://github.com/shofiqtest"><img alt="GitHub" src="https://img.shields.io/badge/GitHub-shofiqtest-181717?style=for-the-badge&logo=github&logoColor=white"></a>

Espoo, Finland — Open to Linux / embedded roles in Europe and remote

</div>

---

## Linux Kernel Contributions

Active upstream contributor across IIO, networking, sound, SoC, SCSI, power supply, XFS, and MFD — **13 patches, 8 subsystems, 9 merged**. Full patch history on [lore.kernel.org](https://lore.kernel.org/all/?q=Md+Shofiqul+Islam).

| Patch | Subsystem | Status |
| --- | --- | --- |
| [`iio: adc: ti-ads1298: Remove incorrect test signal init`](https://www.spinics.net/lists/kernel/msg6192186.html) | IIO / Medical ADC | ✅ **Applied** — functional bug fix · Jonathan Cameron · confirmed by Mike Looijmans & David Lechner |
| [`iio: adc: ti-ads1298: Fix incorrect timeout comment`](https://lore.kernel.org/linux-iio/?q=ti-ads1298+timeout+shofiqtest) | IIO / Medical ADC | ✅ **Applied** — Jonathan Cameron · iio/togreg |
| [`iio: adc: ti-ads1298: Add parentheses around macro parameter`](https://www.spinics.net/lists/kernel/msg6191377.html) | IIO / Medical ADC | ✅ **Applied** — Jonathan Cameron · iio/togreg |
| [`sctp: Fix typo in comment`](https://git.kernel.org/netdev/net-next/c/c7ea0d2b4d76) | Networking / SCTP | ✅ **Merged** — `netdev/net-next` · applied by Jakub Kicinski · [`c7ea0d2b4d76`](https://git.kernel.org/netdev/net-next/c/c7ea0d2b4d76) |
| [`ASoC: nau8825: Fix typos in comments`](https://git.kernel.org/broonie/sound/c/5f1752afb464) | Sound / ASoC | ✅ **Merged** — `broonie/sound for-7.2` · queued for Linux 7.2 |
| [`xfs: Fix typo in comment`](https://www.spinics.net/lists/kernel/msg6190059.html) | XFS Filesystem | ✅ **Accepted** — Carlos Maiolino · `for-next` · [`509fdeb3326b`](https://git.kernel.org/pub/scm/linux/kernel/git/djwong/xfs-linux.git) |
| [`scsi: scsi_scan: Fix typo in comment`](https://www.spinics.net/lists/kernel/msg6189223.html) | SCSI core | ✅ **Applied** — `7.2/scsi-staging` · Martin K. Petersen · `Reviewed-by: Bart Van Assche` |
| [`scsi: storvsc: Replace symbolic permissions with octal`](https://www.spinics.net/lists/kernel/msg6188547.html) | SCSI / Hyper-V | ✅ **Applied** — `7.2/scsi-staging` · Martin K. Petersen · `Reviewed-by: Long Li` (Microsoft) |
| [`power: supply: Fix typos in comments`](https://www.spinics.net/lists/kernel/msg6189221.html) | Power Supply | 🔄 v2 sent — `Acked-by: Linus Walleij` · awaiting maintainer |
| [`soc: ti: knav_qmss_queue: Implement resource cleanup in remove()`](https://www.spinics.net/lists/kernel/msg6189942.html) | SoC / TI Keystone | ✅ **Applied** — `ti-drivers-soc-next` · Nishanth Menon · commit `10a1969353b2` · queued for linux-next |
| [`mfd: si476x-i2c: Fix spelling mistakes in comments`](https://lore.kernel.org/linux-mfd/20260514181954.1442-1-shofiqtest@gmail.com/) | MFD / Silicon Labs Si476x radio | 🔄 **Under review** — v2 with `Signed-off-by` submitted · awaiting Lee Jones |
| [`iio: accel: adxl372: Add timestamp to FIFO data`](https://lore.kernel.org/linux-iio/20260516211935.36773-1-shofiqtest@gmail.com/) | IIO / MEMS accelerometer | 🔄 **Under review** — v2 · `IIO_DECLARE_BUFFER_WITH_TS` + `iio_push_to_buffers_with_ts()` · per David Lechner review |

## Networking & Data Center Open Source

### SONiC (Software for Open Networking in the Cloud)

SONiC is the open-source Linux-based NOS powering data-center switches at Microsoft, Cisco, Arista, and others.

| Patch | Component | Status |
| --- | --- | --- |
| [`pfcwd: fix TypeError crash in interval() on partial PFC_WD entries`](https://github.com/sonic-net/sonic-utilities/pull/4541) | PFC Watchdog CLI — `pfcwd/main.py` · `sonic-net/sonic-utilities` | 🔄 **Open** — DCO ✅ · EasyCLA ✅ · [PR #4541](https://github.com/sonic-net/sonic-utilities/pull/4541) |

`pfc_stat_history_cmd` creates partial `PFC_WD` entries with no `detection_time`/`restoration_time`. `interval()` called `int(None)` unconditionally, crashing and permanently blocking polling-interval updates. Fix guards before conversion, skips incomplete entries, and consolidates redundant DB reads. Includes regression test.

### DPDK (Data Plane Development Kit)

DPDK is the high-performance packet-processing framework used in data centers, 5G, and networking infrastructure — same `git send-email` workflow as the Linux kernel.

| Patch | Component | Status |
| --- | --- | --- |
| [`bus/fslmc: fix ignored return value in fslmc_bus_unplug`](https://inbox.dpdk.org/dev/20260513203725.1905-2-shofiqtest@gmail.com/) | NXP DPAA2 bus driver — `drivers/bus/fslmc/fslmc_bus.c` | 🔄 **Under review** — `dev@dpdk.org` · CC: Hemant Agrawal, Sachin Saxena (NXP) |
| [`dma/dpaa2: fix dpaa2_qdma_remove always returning success`](https://inbox.dpdk.org/dev/20260513203725.1905-3-shofiqtest@gmail.com/) | NXP DPAA2 DMA driver — `drivers/dma/dpaa2/dpaa2_qdma.c` | 🔄 **Under review** — `dev@dpdk.org` · CC: Gagandeep Singh, Hemant Agrawal (NXP) |

`fslmc_bus_unplug()` discarded `drv->remove()` return value, always reporting success. `dpaa2_qdma_remove()` logged errors but returned `0`, hiding failures from callers. Fixes [Bugzilla #1914](https://bugs.dpdk.org/show_bug.cgi?id=1914). Both patches tagged `Cc: stable@dpdk.org`.

### U-Boot (i.MX6Q bootloader — GE Healthcare medical device platform)

U-Boot is the bootloader used in embedded Linux systems including NXP i.MX6Q-based medical devices (patient monitors, ultrasound, imaging).

| Contribution | Component | Status |
| --- | --- | --- |
| [SPL overflow fix for `clk: imx6q` patch series](https://lore.kernel.org/all/CAOMZO5De=9ECdSZ=VxvhrAJxRX7vpHu65hCueUn7VChmBnYPxQ@mail.gmail.com/) | `drivers/clk/imx/clk-imx6q.c` — guard `of_assigned_ldb_sels()` and `imx6q_init_ldb_clks()` with `!CONFIG_SPL_BUILD` | 🔄 **Sent to maintainer** — fix for CI failure reported by Fabio Estevam · CC: Brian Ruley (GE Healthcare Finland) |

Diagnosed and fixed an SPL SRAM overflow (112 bytes) caused by LDB display clock initialisation code being pulled into SPL via `imx6q_clk_probe()`. SPL never initialises a display — guarding the two functions reduces SPL text by ~688 bytes and unblocks the patch series.

## Quantum Computing Contributions

| Contribution | Project | Status |
| --- | --- | --- |
| [`docs: add Advantage2 mention alongside Advantage in overview`](https://github.com/dwavesystems/dwave-ocean-sdk/pull/453) | D-Wave Ocean SDK — quantum annealing platform docs | ✅ **Merged** — merged by Joel Pasvolsky · PR #453 · `cd94d3c` |

## Zephyr RTOS Contributions

| Contribution | Area | Status |
| --- | --- | --- |
| [`drivers: sensor: max3010x: MAX30101/MAX30102 driver`](https://github.com/zephyrproject-rtos/zephyr/pull/108697) | Sensor driver, I2C, Devicetree binding, Kconfig, build coverage | ✅ **Merged** — merged by Benjamin Cabé · approved by Jilay Pandya & Maureen Helm · [PR #108697](https://github.com/zephyrproject-rtos/zephyr/pull/108697) |
| `maxim,max3010x-common` shared DT binding | Maxim pulse oximeter / heart-rate sensor family | ✅ **Merged** — extracted into shared binding per maintainer review |
| `tests/drivers/build_all/sensor/i2c.dtsi` coverage | Zephyr sensor build test matrix | ✅ **Merged** — added per maintainer review |

## Systems I Like Working On

| Domain | Tools and technologies |
| --- | --- |
| Kernel and BSP | Linux kernel, device drivers, DTS, Kconfig, Makefiles |
| Embedded and RTOS | Zephyr RTOS, C, C++, sensor interfaces, I2C/SPI |
| Runtime and platform | SoC software, debugging, CI, performance-minded systems work |
| Networking and DC | DPDK, SONiC, data-centre switch software, high-performance packet processing |
| Cloud-adjacent engineering | Docker, Kubernetes, Azure AKS, monitoring, automation |

## Tools I Use

<p>
  <img alt="Linux Kernel" src="https://img.shields.io/badge/Linux_Kernel-FCC624?style=flat-square&logo=linux&logoColor=black">
  <img alt="C" src="https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white">
  <img alt="C++" src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=c%2B%2B&logoColor=white">
  <img alt="Python" src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white">
  <img alt="Bash" src="https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnu-bash&logoColor=white">
  <img alt="Zephyr" src="https://img.shields.io/badge/Zephyr_RTOS-0F172A?style=flat-square">
  <img alt="DPDK" src="https://img.shields.io/badge/DPDK-contributor-555555?style=flat-square">
  <img alt="SONiC" src="https://img.shields.io/badge/SONiC-contributor-0078D4?style=flat-square">
  <img alt="CMake" src="https://img.shields.io/badge/CMake-064F8C?style=flat-square&logo=cmake&logoColor=white">
  <img alt="Git" src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white">
  <img alt="GitHub Actions" src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=github-actions&logoColor=white">
  <img alt="Docker" src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white">
  <img alt="Kubernetes" src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white">
  <img alt="QEMU" src="https://img.shields.io/badge/QEMU-FF6600?style=flat-square&logo=qemu&logoColor=white">
  <img alt="checkpatch" src="https://img.shields.io/badge/checkpatch-passing-brightgreen?style=flat-square">
  <img alt="git send-email" src="https://img.shields.io/badge/git_send--email-active-orange?style=flat-square">
  <img alt="lore.kernel.org" src="https://img.shields.io/badge/lore.kernel.org-contributor-blue?style=flat-square">
  <img alt="sparse" src="https://img.shields.io/badge/sparse-clean-brightgreen?style=flat-square">
</p>

## Education

- **M.HSc. Biomedical Engineering** — [University of Oulu](https://www.oulu.fi/en/), Finland (2016–2021)
- **M.Sc. Computer Science & Engineering** — [Islamic University](https://www.iu.ac.bd/), Kushtia, Bangladesh (2014–2015)
- **B.Sc. Electrical & Electronics Engineering** — [International Islamic University Chittagong](https://www.iiuc.ac.bd/), Bangladesh (2008–2013)

## Certifications

- Linux for Engineers — The Linux Foundation
- Introduction to RISC-V (LFD110) — The Linux Foundation
- Generative AI and Large Language Models — Coursera

## Featured Projects

| Project | What it shows |
| --- | --- |
| [Real-Time Patient Monitoring on Kubernetes](https://github.com/shofiqtest/real-time-patient-monitoring-k8s) | Cloud-native monitoring architecture |
| Embedded driver work | Low-level C, hardware-facing debugging, upstream workflow |

## GitHub Snapshot

<p align="center">
  <img height="165" alt="GitHub stats" src="https://github-readme-stats.vercel.app/api?username=shofiqtest&show_icons=true&theme=tokyonight&hide_border=true" />
  <img height="165" alt="Top languages" src="https://github-readme-stats.vercel.app/api/top-langs/?username=shofiqtest&layout=compact&theme=tokyonight&hide_border=true" />
</p>

<p align="center">
  <img alt="GitHub streak" src="https://streak-stats.demolab.com?user=shofiqtest&theme=tokyonight&hide_border=true" />
</p>
