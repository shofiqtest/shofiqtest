<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1a1a2e,50:4a235a,100:0a3d62&height=200&section=header&text=Hi%20there%2C%20I%27m%20Shofiq%20%F0%9F%91%8B&fontSize=44&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Linux%20Kernel%20Contributor%20%C2%B7%20SoC%20SW%20Engineer%20%40Nokia%20%C2%B7%20C%2FC%2B%2B%20Systems%20%26%20Runtime&descSize=17&descAlignY=58&descColor=c8b8ff" width="100%"/>
</div>

<br/>

<table width="100%" border="0" cellspacing="0" cellpadding="0">
<tr>
<td valign="top" width="60%">

### 🐧 Upstream Linux Kernel Contributor
**Networking · IIO · ASoC · SCSI · SoC · XFS · Power Supply**

Patches reviewed and applied by subsystem maintainers including **Jakub Kicinski** (net-next), **Mark Brown** (ASoC), and **Darrick J. Wong** (XFS).

- 🔴 **SCTP patch merged** → `netdev/net-next` by Jakub Kicinski
- ✅ **ASoC patch merged** → queued for Linux 7.2
- ✅ **IIO 3-patch series merged** → `iio/togreg`

</td>
<td valign="top" align="center" width="40%">
<img src="https://capsule-render.vercel.app/api?type=rect&color=0:1a1a2e,100:0a3d62&height=200&section=header&text=%3C%2F%3E%0ALinus%20Torvalds%20%3A%20Talk%20is%20cheap.%0AShow%20me%20the%20code.&fontSize=13&fontColor=7ec8e3&animation=fadeIn&fontAlignY=50" width="100%" height="200"/>
</td>
</tr>
</table>

---

## 📬 Contact — Open to Senior Linux / Embedded Roles in Europe & Remote

> **Recruiters & Hiring Teams:** best way to reach me is **email or LinkedIn** below.

<div align="center">

[![Email](https://img.shields.io/badge/📧%20Email-shofiqtest%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:shofiqtest@gmail.com)
&nbsp;
[![LinkedIn](https://img.shields.io/badge/💼%20LinkedIn-Md%20Shofiqul%20Islam-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mdshofiqul/)
&nbsp;
[![Kernel Patches](https://img.shields.io/badge/🐧%20Kernel%20Patches-lore.kernel.org-F8C517?style=for-the-badge&logo=linux&logoColor=black)](https://lore.kernel.org/all/?q=Md+Shofiqul+Islam)

</div>

📍 Espoo, Finland &nbsp;·&nbsp; Open to relocation (Ireland, EU) or fully remote

---

## 🐧 Linux Kernel Upstream Contributions

<div align="center">

🔗 **All patches publicly visible:** &nbsp; [![lore.kernel.org](https://img.shields.io/badge/lore.kernel.org-Md%20Shofiqul%20Islam-F8C517?style=for-the-badge&logo=linux&logoColor=black)](https://lore.kernel.org/all/?q=Md+Shofiqul+Islam)

</div>

Active upstream contributor — full patch lifecycle: `checkpatch`, `git send-email`, maintainer review, v2/v3 iterations, subsystem tree tracking.

<div align="center">

| Patch | Subsystem | Status |
|:------|:---------:|-------:|
| `sctp: Fix typo in comment` | Networking / SCTP | ✅ **[Merged → netdev/net-next](https://git.kernel.org/netdev/net-next/c/c7ea0d2b4d76)** applied by Jakub Kicinski |
| `ASoC: nau8825: Fix typos in comments` | Sound / ASoC | ✅ **Merged → Linux 7.2** (broonie/sound.git) |
| `iio: adc: ti-ads1298: Three driver cleanups` | IIO / Medical ECG ADC | ✅ **Merged → iio/togreg** (Acked-by Mike Looijmans) |
| `soc: ti: knav_qmss_queue: Resource cleanup` | SoC / TI Keystone | 📬 v2 — Suggested-by Nishanth Menon (TI) |
| `scsi: storvsc: Replace symbolic permissions` | SCSI / Hyper-V | 📬 v2 — Reviewed-by Long Li (Microsoft) |
| `power: supply: Fix typos in comments` | Power Supply | 📬 Acked-by Linus Walleij |
| `xfs: Fix typo in comment` | XFS Filesystem | 📬 Reviewed-by Darrick J. Wong |

</div>

---

## 🦅 Zephyr RTOS — Upstream Sensor Driver (In Review)

| PR | Description | Status |
|:---|:------------|:------:|
| [**drivers: sensor: max30101: Add MAX30102 support**](https://github.com/zephyrproject-rtos/zephyr/pull/108697) | I2C pulse oximeter driver · YAML DT bindings · Kconfig hierarchy | 📬 Under review |

New `maxim,max30102` compatible added to the existing max30101 driver — YAML Device Tree binding design (`maxim,max3010x-common.yaml`), Kconfig restructuring, compile-test coverage. Build verified in `zephyrprojectrtos/ci` Docker container (498/498 steps, zero errors).

---

## ⚙️ Core Expertise

```
Linux Kernel    ████████████████░░░░  Networking, IIO, SCSI, SoC, ASoC, XFS, SCTP
Zephyr RTOS     ████████████░░░░░░░░  Sensor drivers, Devicetree bindings, west build system
C / C++17       ████████████████████  5+ years — Nokia SoC runtime, embedded systems
Concurrency     ████████████████████  Lock-free queues, atomics, spinlocks, POSIX threads
Performance     ████████████████░░░░  perf profiling, cache optimisation, benchmarking
Embedded Linux  ████████████████░░░░  Yocto, Bitbake, cross-compilation, Wind River
Python          ████████████░░░░░░░░  Test automation, Robot Framework, CI/CD pipelines
```

---

## 🚀 Featured Projects

### ⚡ High-Performance C++ Event Engine
> Lock-free MPMC queue &nbsp;·&nbsp; **8–12M events/sec** &nbsp;·&nbsp; **1–5μs latency** &nbsp;·&nbsp; perf profiled

[![Repo](https://img.shields.io/badge/GitHub-high--performance--event--engine-181717?style=for-the-badge&logo=github)](https://github.com/shofiqtest/high-performance-event-engine)

- 64-byte cache-line alignment, false sharing elimination, atomic CAS operations
- Benchmarked across 4 producer / 4 consumer threads with `perf`

### 🏥 Real-Time Patient Monitoring on Kubernetes
> FastAPI &nbsp;·&nbsp; TimescaleDB &nbsp;·&nbsp; Redis &nbsp;·&nbsp; Azure AKS

[![Repo](https://img.shields.io/badge/GitHub-real--time--patient--monitoring--k8s-181717?style=for-the-badge&logo=github)](https://github.com/shofiqtest/real-time-patient-monitoring-k8s)

---

## 🛠️ Tech Stack

<div align="center">

**Kernel & Languages**

![Linux](https://img.shields.io/badge/Linux_Kernel-FCC624?style=flat-square&logo=linux&logoColor=black)
![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=c%2B%2B&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnu-bash&logoColor=white)

**Build & Tooling**

![CMake](https://img.shields.io/badge/CMake-064F8C?style=flat-square&logo=cmake&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=github-actions&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![QEMU](https://img.shields.io/badge/QEMU-FF6600?style=flat-square&logo=qemu&logoColor=white)

**Upstream Kernel Workflow**

![checkpatch](https://img.shields.io/badge/checkpatch-passing-brightgreen?style=flat-square)
![git send-email](https://img.shields.io/badge/git_send--email-active-orange?style=flat-square)
![lore.kernel.org](https://img.shields.io/badge/lore.kernel.org-contributor-blue?style=flat-square)
![sparse](https://img.shields.io/badge/sparse-clean-brightgreen?style=flat-square)

</div>

---

## 📊 GitHub Stats

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=shofiqtest&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&include_all_commits=true" height="165"/>
  &nbsp;
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=shofiqtest&layout=compact&theme=tokyonight&hide_border=true&langs_count=6" height="165"/>
</div>

---

## 🎓 Education

- 🎓 **M.HSc. Biomedical Engineering** — University of Oulu, Finland (2016–2021)
- 🎓 **M.Sc. Computer Science & Engineering** — Islamic University, Bangladesh (2014–2015)
- 🎓 **B.Sc. Electrical & Electronics Engineering** — IIUC, Bangladesh (2008–2013)

---

## 🏅 Certifications

- Linux for Engineers — The Linux Foundation
- Introduction to RISC-V (LFD110) — The Linux Foundation
- Generative AI and Large Language Models — Coursera

---

<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0a3d62,50:4a235a,100:1a1a2e&height=100&section=footer" width="100%"/>
</div>
