# Cloud Hypervisor Linux Fork

Contains patches for:

* Support for virtio-watchdog
* Boot time performance reporting for x86_64

The arm64 kernel does not write to Cloud Hypervisor's boot-timing MMIO register
at `0x09000f00`: the address is unmapped on other hypervisors, including Apple's
Virtualization.framework, where the write prevents booting on macOS 27.

