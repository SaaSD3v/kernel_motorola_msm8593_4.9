# Moto Z2 Play (albus) Linux 4.9 provenance

This branch is based directly on the original public Linux 4.9 Albus tree:

- Upstream repository: `marcost2/kernel_motorola_msm8593_4.9`
- Upstream base used here: `9f7458ae94af543b42d9ce03ff66cb2e768acc25`
- The upstream history is retained as ancestry; it is not squashed or re-authored.

Key Albus 4.9 bring-up commits retained with their original author, **marcost2**:

- `3fda10145bcda087e8a59caee566a51623f754aa` — `arm64: Import albus dts`
- `631742a7f686cd41fcfbcd0d90cfc61f7d26da38` — `arm64: albus: Forward ports dtb's`
- `9710a7cf95e8a938cf5553e776bad32a865302a6` — `arm64: configs: Add albus defconfig`
- `13b91fee2d5723e6e27eda1c1b1d27ad62233513` — `arch: arm64: Update albus NFC pinctrl`

The tree also retains Motorola, Cirrus Logic, Qualcomm/Linux and other authors in the original commit history and `Signed-off-by` trailers. Their work must not be presented as SaaSD3v-authored work.

DroidSpaces-specific changes are layered on top. The cgroup noprefix adaptation is committed with the original patch author (`ravindu644 <droidcasts@protonmail.com>`). The Android network capability adaptation is committed with its original author (`SaaSD3v <hearesaas@gmail.com>`). Albus build fixes discovered during this integration are separate commits and are not attributed to the upstream Albus 4.9 authors.
