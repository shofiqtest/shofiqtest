<p align="center">
  <img src="./assets/profile-card.svg" alt="Md Shofiqul Islam - Linux kernel and embedded systems profile card" width="100%" />
</p>

## Linux Kernel Contributions

Active upstream contributor across networking, sound, IIO, SoC, SCSI, power supply, and XFS. Public patch history is available on [lore.kernel.org](https://lore.kernel.org/all/?q=Md+Shofiqul+Islam) and [spinics.net](https://www.spinics.net/lists/kernel/).

| Patch | Subsystem | Current status |
| --- | --- | --- |
| [`sctp: Fix typo in comment`](https://git.kernel.org/netdev/net-next/c/c7ea0d2b4d76) | Networking / SCTP | Merged to `netdev/net-next` by Jakub Kicinski |
| `ASoC: nau8825: Fix typos in comments` | Sound / ASoC | Applied to `broonie/sound.git`, queued for Linux 7.2 |
| [`iio: adc: ti-ads1298: Add parentheses around macro parameter`](https://www.spinics.net/lists/kernel/msg6191377.html) | IIO / Medical ADC | v2 under maintainer review |
| [`iio: adc: ti-ads1298: Fix incorrect timeout comment`](https://www.spinics.net/lists/kernel/msg6192178.html) | IIO / Medical ADC | v2 under maintainer review |
| [`iio: adc: ti-ads1298: Remove unnecessary CONFIG2 write during init`](https://www.spinics.net/lists/kernel/msg6192186.html) | IIO / Medical ADC | v2 reviewed positively; waiting on series follow-up |
| [`soc: ti: knav_qmss_queue: Implement resource cleanup in remove()`](https://www.spinics.net/lists/kernel/msg6189942.html) | SoC / TI Keystone | v2 submitted; `Suggested-by: Nishanth Menon` |
| [`scsi: storvsc: Replace symbolic permissions with octal`](https://www.spinics.net/lists/kernel/msg6188547.html) | SCSI / Hyper-V | v2 submitted after review feedback |
| [`scsi: scsi_scan: Fix typo in comment`](https://www.spinics.net/lists/kernel/msg6189223.html) | SCSI core | v2 submitted after review feedback |
| [`power: supply: Fix typos in comments`](https://www.spinics.net/lists/kernel/msg6189221.html) | Power Supply | v2 submitted with `Acked-by: Linus Walleij` |
| [`xfs: Fix typo in comment`](https://www.spinics.net/lists/kernel/msg6190059.html) | XFS Filesystem | v2 submitted with `Reviewed-by: Darrick J. Wong` |

## Zephyr RTOS Contributions

I work on embedded Linux and RTOS driver development, with recent focus on sensor drivers, board bring-up, Devicetree bindings, Kconfig, and upstream-quality C code.

| Contribution | Area | Current status |
| --- | --- | --- |
| [`drivers: sensor: max30101: Add MAX30102 support`](https://github.com/zephyrproject-rtos/zephyr/pull/108697) | Sensor driver, I2C, Devicetree binding, Kconfig, build coverage | Open; changes requested; CI checks green |
| `maxim,max30102` compatible support | Maxim pulse oximeter / heart-rate sensor family | Under review in PR #108697 |
| `tests/drivers/build_all/sensor/i2c.dtsi` coverage | Zephyr sensor build test matrix | Added in response to maintainer review |

## Systems I Like Working On

| Domain | Tools and technologies |
| --- | --- |
| Kernel and BSP | Linux kernel, device drivers, DTS, Kconfig, Makefiles |
| Embedded and RTOS | Zephyr RTOS, C, C++, sensor interfaces, I2C/SPI |
| Runtime and platform | SoC software, debugging, CI, performance-minded systems work |
| Cloud-adjacent engineering | Docker, Kubernetes, Azure AKS, monitoring, automation |

## Tools I Use

<p>
  <img alt="Linux Kernel" src="https://img.shields.io/badge/Linux_Kernel-FCC624?style=flat-square&logo=linux&logoColor=black">
  <img alt="C" src="https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white">
  <img alt="C++" src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=c%2B%2B&logoColor=white">
  <img alt="Python" src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white">
  <img alt="Bash" src="https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnu-bash&logoColor=white">
  <img alt="Zephyr" src="https://img.shields.io/badge/Zephyr_RTOS-0F172A?style=flat-square">
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

- **M.HSc. Biomedical Engineering** - University of Oulu, Finland (2016-2021)
- **M.Sc. Computer Science & Engineering** - Islamic University, Bangladesh (2014-2015)
- **B.Sc. Electrical & Electronics Engineering** - IIUC, Bangladesh (2008-2013)

## Certifications

- Linux for Engineers - The Linux Foundation
- Introduction to RISC-V (LFD110) - The Linux Foundation
- Generative AI and Large Language Models - Coursera

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
