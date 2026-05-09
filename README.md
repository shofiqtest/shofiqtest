# Hi there, I'm Shofiq 👋

**Linux Kernel Contributor** · **Zephyr RTOS Contributor** · **SoC Software Engineer at Nokia** · **C/C++ Systems & Runtime**

---

## 📫 Contact — Open to Senior Linux / Embedded Roles in Europe & Remote

> **Recruiters:** best way to reach me is email or LinkedIn below.

[![Email](https://img.shields.io/badge/Email-shofiqtest%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:shofiqtest@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Md_Shofiqul_Islam-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mdshofiqul/)
[![Kernel Patches](https://img.shields.io/badge/Kernel_Patches-lore.kernel.org-F8C517?style=for-the-badge&logo=linux&logoColor=black)](https://lore.kernel.org/all/?q=Md+Shofiqul+Islam)

📍 Espoo, Finland · Open to relocation (Ireland, EU) or fully remote

---

## 🐧 Linux Kernel Contributions

Active upstream contributor — patches reviewed, accepted, and queued for mainline:

| Patch | Subsystem | Status |
|-------|-----------|--------|
| `sctp: Fix typo in comment` | Networking / SCTP | ✅ **Merged → netdev/net-next** ([c7ea0d2b4d76](https://git.kernel.org/netdev/net-next/c/c7ea0d2b4d76)) applied by Jakub Kicinski |
| `ASoC: nau8825: Fix typos in comments` | Sound / ASoC | ✅ Applied → Linux 7.2 (broonie/sound.git) |
| `iio: adc: ti-ads1298: Three driver cleanups` | IIO / Medical ECG ADC | ✅ Merged → iio/togreg (Acked-by Mike Looijmans) |
| `soc: ti: knav_qmss_queue: Implement resource cleanup` | SoC / TI Keystone | 📬 v2 — Suggested-by Nishanth Menon (TI) |
| `scsi: storvsc: Replace symbolic permissions with octal` | SCSI / Hyper-V | 📬 v2 — Reviewed-by Long Li (Microsoft) |
| `power: supply: Fix typos in comments` | Power Supply | 📬 Acked-by Linus Walleij |
| `xfs: Fix typo in comment` | XFS Filesystem | 📬 Reviewed-by Darrick J. Wong |

🔗 [All patches on lore.kernel.org](https://lore.kernel.org/all/?q=Md+Shofiqul+Islam)

---

## 🦅 Zephyr RTOS Contributions

Extending sensor drivers for medical IoT devices:

| PR | Subsystem | Status |
|----|-----------|--------|
| [drivers: sensor: max30101: Add MAX30102 support](https://github.com/zephyrproject-rtos/zephyr/pull/108697) | Sensors / Devicetree | 📬 Under review |

The MAX30102 is a pulse oximeter and heart rate sensor (Red + IR LEDs). Added as a second `DT_DRV_COMPAT` in the existing max30101 driver — new DT binding, runtime Green LED guard, shared Kconfig for triggers and die temperature.

---

## 💡 What I Do

- Write **upstream Linux kernel patches** — full workflow: `checkpatch`, `git send-email`, maintainer review cycles, v2/v3 iterations
- Develop **performance-critical C/C++ runtime software** for SoC/FPGA platforms at Nokia (5G beamforming systems)
- Design **thread-safe concurrent components**: lock-free queues, atomic operations, hardware abstraction layers
- Contribute to **medical device drivers** (IIO health subsystem — ECG ADCs, pulse oximeters) backed by a Biomedical Engineering degree

---

## ⚙️ Core Expertise

```
Linux Kernel    ████████████████░░░░  Upstream contributor (Networking, IIO, SCSI, SoC, ASoC, XFS, SCTP)
Zephyr RTOS     ████████████░░░░░░░░  Sensor drivers, Devicetree bindings, west build system
C / C++17       ████████████████████  5+ years, Nokia SoC runtime systems
Concurrency     ████████████████████  Lock-free, atomics, spinlocks, POSIX threads
Performance     ████████████████░░░░  Profiling, cache optimization, benchmarking
Embedded Linux  ████████████████░░░░  Yocto, Bitbake, cross-compilation, Wind River
Python          ████████████░░░░░░░░  Automation, tooling, CI/CD pipelines
```

---

## 🔬 Medical Device Background

**M.HSc. Biomedical Engineering** (University of Oulu) + thesis at **Sooma Medical**

Applying domain knowledge to Linux kernel IIO health drivers:

- **TI ADS1298** — 8-channel medical ECG ADC driver (`drivers/iio/adc/`)
- **MAX30102** — pulse oximeter / heart rate sensor (`drivers/iio/health/`)
- **Melexis MLX90632** — medical-grade contactless IR thermometer

---

## 🚀 Featured Projects

### ⚡ High-Performance C++ Event Engine
> Lock-free MPMC queue · **8–12M events/sec** · **1–5μs latency** · Deployed on AKS

[![Repo](https://img.shields.io/badge/GitHub-high--performance--event--engine-181717?logo=github)](https://github.com/shofiqtest/high-performance-event-engine)

- Lock-free MPMC queue with 64-byte cache-line alignment and false sharing elimination
- Atomic CAS operations, zero-copy design
- Benchmarked with perf across 4 producer / 4 consumer threads

### 🏥 Real-Time Patient Monitoring on Kubernetes
> Distributed backend · FastAPI · TimescaleDB · Redis · Azure AKS

[![Repo](https://img.shields.io/badge/GitHub-real--time--patient--monitoring--k8s-181717?logo=github)](https://github.com/shofiqtest/real-time-patient-monitoring-k8s)

---

## 🛠️ Tech Stack

**Kernel & Systems**

![Linux](https://img.shields.io/badge/Linux_Kernel-FCC624?logo=linux&logoColor=black)
![C](https://img.shields.io/badge/C-00599C?logo=c&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?logo=c%2B%2B&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)

**Build & Tooling**

![CMake](https://img.shields.io/badge/CMake-064F8C?logo=cmake&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?logo=git&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?logo=github-actions&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)

**Kernel Workflow**

![checkpatch](https://img.shields.io/badge/checkpatch-passing-brightgreen)
![git send-email](https://img.shields.io/badge/git_send--email-workflow-orange)
![lore.kernel.org](https://img.shields.io/badge/lore.kernel.org-contributor-blue)

---

## 📊 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=shofiqtest&show_icons=true&theme=dark&hide_border=true&count_private=true" height="165"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=shofiqtest&layout=compact&theme=dark&hide_border=true" height="165"/>
</p>

---

## 🎓 Education

- **M.HSc. Biomedical Engineering** — University of Oulu, Finland
- **M.Sc. Computer Science & Engineering** — Islamic University, Kushtia, Bangladesh
- **B.Sc. Electrical & Electronics Engineering** — International Islamic University Chittagong, Bangladesh
