<div align="center">

# Md Shofiqul Islam

**Embedded Linux and SoC Software Engineer | System Design**

Espoo, Finland &nbsp;·&nbsp; Open to roles in Europe (Ireland · Germany · Netherlands · Sweden)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-mdshofiqul-0A66C2?style=flat&logo=linkedin)](https://www.linkedin.com/in/mdshofiqul/)
[![Kernel Patches](https://img.shields.io/badge/Linux%20Kernel-15%20patches%20merged-F8A800?style=flat&logo=linux&logoColor=white)](https://lore.kernel.org/all/?q=Md+Shofiqul+Islam)
[![DPDK](https://img.shields.io/badge/DPDK-26.07%20new%20contributor-0A7D43?style=flat)](https://mails.dpdk.org/archives/announce/2026-July/000565.html)
[![Website](https://img.shields.io/badge/Website-kernel--medical.github.io-4CAF50?style=flat&logo=github)](https://kernel-medical.github.io)

**[Embedded Linux & Medical Software Portfolio](https://kernel-medical.github.io/linux-medical-bsp/)**

</div>

---

## What I work on

I am an embedded Linux and SoC software engineer based in Espoo, Finland. At Nokia, I worked on C/C++ platform and signal-processing software for real-time 5G RF/L1 systems. My work included a channel-estimation library, hardware integration, RTOS/Linux debugging and Python tools for validation.

I also contribute to Linux, Zephyr, U-Boot and DPDK. My patches cover sensor drivers, error handling and resource cleanup. Alongside this, I build personal projects around medical sensors, ROS 2 and Python applications. You can find the repositories and contribution links further down this page.

---

## From Board Bring-Up to Application Software

My work spans the path from a board starting up to the application using its data. At the platform level, that means board bring-up, U-Boot, Device Tree, Yocto/OpenEmbedded BSPs and device drivers. Above that, I work with C/C++ libraries, real-time software, system services and the interfaces between components.

System design is part of this work: deciding how data moves, where timing matters, what happens when a component fails and how to test the result. My Nokia experience is in platform software and system debugging. My personal ROS 2 and Python/FastAPI projects extend that work into sensor integration and application services.

---

## Linux Kernel Contributions

| Subsystem | Area | Status |
|---|---|---|
| **IIO** | MAX86150 ECG/PPG biosensor driver (512 lines) | Under review |
| **IIO** | ADS1299 8-channel EEG ADC driver | Under review |
| **DRM/Accel** | AMD Ryzen AI NPU · Intel VPU | Merged |
| **net-next** | Intel igb · iwlwifi driver fixes | Merged |
| **ASoC** | Audio codec driver fixes (nau8825, Atmel) | Merged |
| **SCSI** | Hyper-V storvsc (Microsoft) | Merged |
| **XFS / GFS2** | Filesystem fixes (Red Hat) | Merged |
| **Power supply** | Driver fixes | Merged |
| **SoC / TI** | Keystone resource management | Merged |

Full patch history: [lore.kernel.org/all/?q=Md+Shofiqul+Islam](https://lore.kernel.org/all/?q=Md+Shofiqul+Islam)

---

## DPDK / Networking Contributions

| Contribution | Area | Public evidence |
|---|---|---|
| NXP DPAA2 bus/DMA fixes | `bus/fslmc`, `dma/dpaa2`, device removal and unplug error paths | [DPDK patch review and test thread](https://mails.dpdk.org/archives/dev/2026-August/342708.html) |
| DPDK contributor listing | DPDK 26.07 release | [Release announcement listing new contributors](https://mails.dpdk.org/archives/announce/2026-July/000565.html) |
| SONiC network OS tooling | PFC Watchdog CLI crash handling and partial `PFC_WD` database entries | GitHub project work |

---

## Zephyr RTOS Contributions

| Driver | Contribution | Status |
|---|---|---|
| MAX30101 | SpO₂ / heart-rate optical sensor driver | [PR #108697](https://github.com/zephyrproject-rtos/zephyr/pull/108697) — Merged |
| INA237 | Power monitor — fix `sample_fetch` in triggered mode | [PR #110094](https://github.com/zephyrproject-rtos/zephyr/pull/110094) — Merged |

Also active reviewing open sensor driver PRs in `drivers/sensor/` — bmp581, bmp180, scd4x, lsm9ds1, sensor shell.

---

## U-Boot Contributions

| Area | Contribution | Status |
|---|---|---|
| `board/ge/common/vpd_reader.c` | Fix `errloc` array size in `verify_bch()` — was allocated with `data_length` entries instead of `ecc_bits`, orders of magnitude larger than needed | [Merged](https://github.com/u-boot/u-boot/commit/d2d005a32b97) |

---

## Quantum Computing Contributions

| Project | Contribution | Status |
|---|---|---|
| **[Qiskit](https://github.com/Qiskit/qiskit)** (IBM Quantum) | [PR #16590](https://github.com/Qiskit/qiskit/pull/16590) — fix UB writing to uninitialized buffers in transpile layout C API; replace `slice::from_raw_parts_mut` over uninit memory with safe `ptr.add(i).write()` | Open |
| **[D-Wave Ocean SDK](https://github.com/dwavesystems/dwave-ocean-sdk)** | [PR #453](https://github.com/dwavesystems/dwave-ocean-sdk/pull/453) — docs: add Advantage2 mention alongside Advantage in overview | Merged |

---

## Tech Stack

I mainly write C and C++, with Python and Bash for automation and tooling.

- **Platforms and drivers:** Embedded Linux, Yocto/OpenEmbedded, U-Boot, Device Tree, Linux IIO and Zephyr RTOS.
- **Networking:** DPDK, NXP DPAA2, SONiC tooling and Linux network drivers.
- **Architecture:** ARM64; RISC-V coursework through the Linux Foundation.
- **Debugging:** GDB, JTAG/SWD, perf, ftrace and eBPF.
- **Build and validation:** Git, GitHub Actions, Jenkins and Python.
- **Application projects:** ROS 2, FastAPI and Docker.

---

## Certifications

- Introduction to RISC-V (LFD110) — The Linux Foundation
- Linux for Engineers — The Linux Foundation
- Generative AI and LLMs — Coursera

---

## Areas I am interested in

I am interested in work where software has to interact closely with hardware: embedded Linux, medical sensors, real-time communications, robotics and networking. I also follow work on AI accelerators, RISC-V and quantum computing hardware.

---

## Featured AI / AIOps Project

### [Evidence-First Incident Agent](https://github.com/shofiqtest/evidence-first-incident-agent)

[![Incident Agent CI](https://github.com/shofiqtest/evidence-first-incident-agent/actions/workflows/ci.yml/badge.svg)](https://github.com/shofiqtest/evidence-first-incident-agent/actions/workflows/ci.yml)

I built this project to explore how an incident-investigation tool can explain a diagnosis using the evidence it collected. It reads synthetic metrics, logs, traces, deployment records and runbooks through a fixed, read-only workflow. The report ranks possible causes, links them to evidence and identifies uncertainty. It can also abstain when there is not enough evidence.

The project has a FastAPI API, a CLI and a Docker setup. It has 40 automated tests and 90% local test coverage. GitHub Actions also builds the container and checks the API.

The default reasoner uses an offline heuristic. There is an optional OpenAI-compatible interface for models served by Ollama or another endpoint. The published evaluation covers 20 synthetic fixtures using the heuristic; the LLM response handling is tested with mocked endpoints.

[Run the demo](https://github.com/shofiqtest/evidence-first-incident-agent#quickstart)

---

## Project Directory

I keep my public projects under [shofiqtest](https://github.com/shofiqtest?tab=repositories) and [kernel-medical](https://github.com/kernel-medical). The list below includes working prototypes, documentation, portfolio pages and earlier ideas.

### Software and engineering projects

| Project | Focus | What is in the repository |
|---|---|---|
| [Evidence-First Incident Agent](https://github.com/shofiqtest/evidence-first-incident-agent) | Python, FastAPI, AI/AIOps | Incident investigation over synthetic telemetry, optional LLM integration, evidence-cited reports, automated evaluation and Docker CI. |
| [High-Performance Event Engine](https://github.com/shofiqtest/high-performance-event-engine) | C++, concurrency, performance | Sensor-event simulation and benchmark with multiple producers and consumers, a bounded atomic queue, and throughput/latency reporting. |
| [Patient Monitoring Prototype](https://github.com/shofiqtest/real-time-patient-monitoring-k8s) | Python, FastAPI, containers | Patient-record APIs, PostgreSQL/Redis integration, and Docker, Kubernetes, Helm and Terraform configurations. |
| [Linux Kernel Patch Archive](https://github.com/shofiqtest/linux-kernel-patches) | C, Linux kernel | Patch files covering driver cleanup, resource handling and a proposed MAX86150 IIO biosensor driver; upstream contribution evidence is linked in the contribution sections. |
| [Route Simulator Concept](https://github.com/shofiqtest/--Route-Simulator) | Geographical simulation concept | README outlining constant-speed movement along a repeating route defined by geographical points. |

### Kernel Medical projects

| Project | Focus | What is in the repository |
|---|---|---|
| [kernel-soup-gen](https://github.com/kernel-medical/kernel-soup-gen) | Python, source analysis | Generates Markdown SOUP record drafts from Linux driver metadata, Kconfig dependencies, maintainer information and Git history. |
| [ros2_iio_medical](https://github.com/kernel-medical/ros2_iio_medical) | C++, ROS 2, Linux IIO | ROS 2 nodes for sysfs polling and triggered-buffer acquisition, with configurable topics, a synthetic sensor simulator and channel-parser tests. |
| [iec62304-embedded-drivers](https://github.com/kernel-medical/iec62304-embedded-drivers) | Software lifecycle documentation | Reference requirements, design, SOUP, FMEA and lifecycle documents for embedded biosensor drivers and ROS 2 integration. |
| [linux-medical-bsp](https://github.com/kernel-medical/linux-medical-bsp) | Embedded Linux portfolio | Landing page describing medical Linux BSP services, related projects and driver case studies. [View the portfolio](https://kernel-medical.github.io/linux-medical-bsp/). |
| [kernel-medical.github.io](https://github.com/kernel-medical/kernel-medical.github.io) | Interactive engineering portfolio | Project and contribution links, with synthetic biosignal visualizations and system architecture. [Visit the site](https://kernel-medical.github.io). |

### Profile and earlier portfolio work

| Repository | Purpose |
|---|---|
| [GitHub Profile](https://github.com/shofiqtest/shofiqtest) | This profile README and project directory. |
| [Earlier Linux Medical BSP Page](https://github.com/shofiqtest/linux-medical-bsp) | Earlier static landing page for the Linux medical software initiative; current projects are maintained under kernel-medical. |

<details>
<summary><strong>Upstream forks and learning repositories</strong></summary>

These are my forks of upstream projects. Links to my patches and reviews are in the contribution sections above.

| Fork | Upstream project | Area |
|---|---|---|
| [linux](https://github.com/shofiqtest/linux) | [Linux](https://github.com/torvalds/linux) | Kernel source and driver development. |
| [zephyr](https://github.com/shofiqtest/zephyr) | [Zephyr RTOS](https://github.com/zephyrproject-rtos/zephyr) | Embedded RTOS and sensor drivers. |
| [u-boot](https://github.com/shofiqtest/u-boot) | [U-Boot](https://github.com/u-boot/u-boot) | Bootloader and platform software. |
| [qiskit](https://github.com/shofiqtest/qiskit) | [Qiskit](https://github.com/Qiskit/qiskit) | Quantum computing SDK. |
| [sonic-utilities](https://github.com/shofiqtest/sonic-utilities) | [SONiC Utilities](https://github.com/sonic-net/sonic-utilities) | Network operating-system command-line tools. |
| [SlicerIGT](https://github.com/shofiqtest/SlicerIGT) | [SlicerIGT](https://github.com/SlicerIGT/SlicerIGT) | Image-guided intervention modules for 3D Slicer. |
| [Medical-Shop-Management](https://github.com/shofiqtest/Medical-Shop-Management) | [Medical-Shop-Management](https://github.com/sanghis96/Medical-Shop-Management) | C++ medical-shop management example. |

</details>

---

<div align="center">
<sub>For embedded software roles or questions about my projects, you can reach me at:</sub><br>
<a href="mailto:shofiqtest@gmail.com">shofiqtest@gmail.com</a>
</div>
