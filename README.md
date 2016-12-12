# linux-nvme

Arch linux kernel plus NVME patches made by Andy Lutomirski 

These patches enable NVME drives to enter lower power states.
In my case (XPS13) it decreases idle usage by 0.5-1watt

To manually compile the Archlinux kernels from here, follow steps:

(1) git clone: https://github.com/damige/linux-nvme.git

(2) go into /src/[kernel you want]

(3) type "makepkg"
-wait until compilation completes-

(4) pacman -U linux-nvme-*

(5) Adjust your bootloader to boot linux-nvme
<br />
<br />
<br />
<br />
To manually patch your own kernel:
4.8:
<br />
Patch using nvmepatch1-V4.patch, nvmepatch2-V4.patch, nvmepatch3-V4.patch.

4.9 (currently testing only):
<br />
Patch using APST.patch, pm_qos1.patch, pm_qos2.patch, pm_qos3.patch, nvme.patch

Also available on AUR: linux-nvme
