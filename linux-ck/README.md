## linux-ck-matteo

This custom linux-ck build is based off of the [linux-ck PKGBUILD on the AUR](https://aur.archlinux.org/packages/linux-ck).
It contains several speed optimizations, targeted towards Intel CPUs (I use a ThinkPad T440p).

Modify the PKGBUILD and the config file to suit your needs.

If you want to modify which patches/modifications are being applied, modify `tune-config`.

On my laptop, the latest 5.10.8 Kernel (+ CK patchset + my own optimizations) gets compiled & installed in about 14 minutes!
(Obviously already having the sources downloaded, because connection speed may vary)

+ Patch features:
	- Disabled AMD & nVidia graphic drivers;
	- Disabled NUMA;
	- Disabled everything applel;
	- Disabled everything related to AMD, nVidia, Google, Chinese companies, and other unnecessary shit;
	- Disabled most of other companies' options (like broadcom, mediatek, qualcomm, etc.)
	- Disabled most of the unused sound cards;
	- Lowered CPU count to "8", because I only have a CPU with 2C4T (and I could lower it even more to "4" but I will leave it as-is);
	- Lowered GPU count to "2", because no person that I know of has more than 2 GPUs (This includes the iGPU + Discrete GPU);
	- Set Kernel compression to LZ4, and disabled other compressions (performance > size).
	- Use `modprobed.db` file to speed-up compilation (checks `~/.config/modprobed.db` and `./modprobed.db`, but prefers the former.)
