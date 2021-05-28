Hardware Support Status
=======================

This is a project to estimate status of hardware support (PCI only) in latest
versions of FreeBSD, OpenBSD and NetBSD systems with the help of
[lists of supported device IDs](https://github.com/bsdhw/Drivers) taking into account [popularity of devices](https://github.com/linuxhw/DevicePopulation).

We determine support status by the following formula:

    Status = (S1*T1 + S2*T2 + ... + Sn*Tn) / (T1 + T2 + ... + Tn)

    Sn — support status of the device (1 — supported, 0 — not supported)

    Tn — total number of device samples

Everyone can contribute to this report by uploading probes of their computers by
the [hw-probe](https://github.com/linuxhw/hw-probe/blob/master/INSTALL.BSD.md) tool:

    hw-probe -all -upload

### Results

Devices — total devices,
FreeBSD — supported in FreeBSD,
OpenBSD — supported in OpenBSD,
NetBSD  — supported in NetBSD.

| PCI Class                    | Devices | FreeBSD | OpenBSD | NetBSD  |
|------------------------------|---------|---------|---------|---------|
| Card reader                  | 8032    | 98.6%   | 98.6%   | 96.6%   |
| Encryption controller        | 6492    | 37.7%   | 52.3%   | 32.7%   |
| **Graphics card**            | 78096   | 88.7%   | 67.7%   | 60.8%   |
| **Net/ethernet**             | 49021   | 99.1%   | 99.6%   | 95.2%   |
| **Net/wireless**             | 37431   | 71.3%   | 61.9%   | 50.3%   |
| Sd host controller           | 9041    | 57.8%   | 21.3%   | 37.5%   |
| Serial controller            | 4058    | 68.3%   | 84.4%   | 76.4%   |
| Smbus                        | 54625   | 91.9%   | 99.9%   | 99.8%   |
| **Sound**                    | 90010   | 81.9%   | 65.7%   | 0.9%    |
| **Storage/ata**              | 47937   | 91.6%   | 40.6%   | 24.4%   |
| **Storage/ide**              | 30205   | 95.5%   | 94.5%   | 89.1%   |
| **Storage/raid**             | 3378    | 95.1%   | 92.6%   | 89.9%   |
| Storage/sas                  | 160     | 98.1%   | 28.7%   | 28.7%   |
| Storage/scsi                 | 147     | 31.3%   | 90.5%   | 91.8%   |

Avg. hardware support in FreeBSD: 86.69%

Avg. hardware support in OpenBSD: 73.24%

Avg. hardware support in NetBSD: 54.12%

