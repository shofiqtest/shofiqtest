## ROS 2 · Medical Robotics

### ros2_iio_medical — Linux IIO to ROS 2 Bridge

Full acquisition stack from analog biosignal sensor to typed ROS 2 topic:

![Architecture](https://raw.githubusercontent.com/shofiqtest/ros2_iio_medical/master/docs/architecture.svg)

| Node | Mode | Use case |
|---|---|---|
| iio_bridge | sysfs polling | Prototyping, low-rate sensors |
| iio_triggered_bridge | epoll + kernel DMA buffer | Production — hardware-timed, no jitter |

Supports **ADS1299** (24-bit 8ch EEG/ECG), **MAX86150** (ECG+PPG), **MAX30102** (SpO2), **ti-ads1298** (ECG) via the standard Linux IIO sysfs interface — no device-specific userspace code.

[shofiqtest/ros2_iio_medical](https://github.com/shofiqtest/ros2_iio_medical) · Apache-2.0 · CI: Ubuntu 22.04 / ROS 2 Humble

---

