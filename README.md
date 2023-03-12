Hardware Support Status
=======================

This is a project to estimate status of hardware support (PCI only) in latest
versions of FreeBSD, OpenBSD and NetBSD systems with the help of
[lists of supported device IDs](https://github.com/bsdhw/Drivers) taking into account [popularity of devices](https://github.com/linuxhw/DevicePopulation).

We determine support status by the following formula:

    Status = (S1*T1 + S2*T2 + ... + Sn*Tn) / (T1 + T2 + ... + Tn)

    Sn - support status of the device (1 - supported, 0 - not supported)

    Tn - total number of device samples

Everyone can contribute to this report by uploading probes of their computers by
the [hw-probe](https://github.com/linuxhw/hw-probe/blob/master/INSTALL.BSD.md) tool:

    hw-probe -all -upload

### Results

Devices - total devices,
FreeBSD - supported in FreeBSD,
OpenBSD - supported in OpenBSD,
NetBSD  - supported in NetBSD.

| PCI Class                    | Devices | FreeBSD | OpenBSD | NetBSD |
|------------------------------|---------|---------|---------|--------|
|                              | 1214    | 1.6%    | 1.6%    | 1.4%    |
| Card reader                  | 668     | 90.9%   | 90.9%   | 89.1%   |
| Co-processor                 | 220     | 65.5%   | 0.5%    | 65.5%   |
| Encryption controller        | 1746    | 32.3%   | 61.3%   | 41.2%   |
| **Graphics card**            | 9567    | 75.4%   | 82%     | 56.2%   |
| **Net/ethernet**             | 2219    | 75.8%   | 72.5%   | 62.9%   |
| **Net/wireless**             | 3356    | 69.8%   | 71.5%   | 53.9%   |
| Sd host controller           | 1277    | 28.5%   | 22.6%   | 9.5%    |
| Signal processing            | 6780    | 31%     | 45.9%   | 4%      |
| Smbus                        | 8655    | 86.3%   | 96%     | 96.3%   |
| **Sound**                    | 9509    | 82.3%   | 66.8%   | 0.3%    |
| **Storage/ata**              | 8171    | 77.9%   | 22.9%   | 14.1%   |
| **Storage/ide**              | 1908    | 93.7%   | 92.5%   | 85.3%   |
| **Storage/raid**             | 618     | 79.4%   | 81.1%   | 68.6%   |
| Storage/sas                  | 225     | 96.4%   | 78.7%   | 78.2%   |
| Storage/scsi                 | 91      | 14.3%   | 58.2%   | 56%     |

Avg. hardware support in FreeBSD: 69.74%

Avg. hardware support in OpenBSD: 63.98%

Avg. hardware support in NetBSD: 39.56%

