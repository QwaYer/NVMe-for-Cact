# 💿 NVMe-for-Cact

<p align="center">
  <img src="https://img.shields.io/badge/version-2.0.0-green.svg?style=for-the-badge" alt="Version: 2.0.0">
  <img src="https://img.shields.io/badge/license-GPLv3-blue.svg?style=for-the-badge" alt="License: GPLv3">
  <img src="https://img.shields.io/badge/arch-i686-red.svg?style=for-the-badge" alt="Arch: i686">
  <img src="https://img.shields.io/badge/format-cctk-green.svg?style=for-the-badge" alt="Output: nvme.cctk">
  <img src="https://img.shields.io/badge/bus-PCI-blue.svg?style=for-the-badge" alt="PCI">
  <img src="https://img.shields.io/badge/irq-MSI--X-brightgreen.svg?style=for-the-badge" alt="MSI-X">
</p>

<p align="center">
  <strong>English.</strong> Out-of-tree <strong>NVMe</strong> driver → <strong><code>nvme.cctk</code></strong> for <strong>pci_load_module</strong>.<br>
  <strong>2.0.0:</strong> migrated from poll-only to <strong>MSI-X</strong> interrupt-driven I/O. Removed <code>pic_mask_line</code>/<code>pic_unmask_line</code>, added <code>msix_alloc_vector</code>/<code>msix_register_handler</code>/<code>pci_msix_enable</code> with fallback to poll mode.<br>
  <strong>Русский.</strong> Драйвер <strong>NVMe</strong> → <strong><code>nvme.cctk</code></strong>.<br>
  <strong>2.0.0:</strong> переведён с режима опроса на прерывания <strong>MSI-X</strong>.
</p>

---

## 🔨 Building

**Recommended — full workspace**

```sh
make -C CactOS-x86_32 iso
```

**Standalone**

```sh
make install   # auto-detects ../CactKernel-x86_32 and ../LocalRepoCactOS
make clean
```

Override paths if needed: `make KERN_ROOT=/custom/path LOCAL_REPO=/custom/path install`.
