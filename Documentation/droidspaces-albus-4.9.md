# DroidSpaces on Moto Z2 Play (albus) - Linux 4.9

This branch targets the Albus Linux 4.9 kernel while keeping Android 8.1/LineageOS 15.1 compatibility in mind.

The 4.9 tree already contains the cgroup v2/default hierarchy implementation (`cgroup2_fs_type`) and cgroup namespace support (`CLONE_NEWCGROUP`). There is no separate `CONFIG_CGROUP2` option to enable. `CONFIG_CGROUPS=y` plus the selected controllers makes the kernel cgroup2-capable.

For Android 8.1, the safe model is hybrid-capable rather than forcing a fully unified v2 boot hierarchy. Oreo init/vendor policy is built around cgroup v1 mounts, so moving every controller to v2 would require userspace/init changes as well.

The DroidSpaces fragment enables the 4.9-era container fundamentals: PID/UTS/IPC/NET/USER namespaces, cgroup pids/device/memory/cpu/cpuset/blk support, OverlayFS, loop devices, VETH/bridge networking and the Android networking compatibility setting.

Linux 4.9 has an early cgroup v2 implementation. It does not have every modern 5.x/6.x cgroup/BPF feature, so DroidSpaces should retain its v1 fallback for features such as modern BPF cgroup-device handling.
