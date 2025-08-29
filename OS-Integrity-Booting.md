# Setting up an OS for Virtualization or Dual Booting

## Downloading an OS
  Usually, you enter an official website and/or a GitHub repository. When you download an operating system,
it becomes an image file initially, which must become bootable for BIOS, or that image can become bootable
if using that OS for a Virtual Machine.

If you plan to do virtualization/VM you'll need to enable the Virtualization option in the BIOS for the 
motherboard and respective CPU (AMD or Intel).

## Partitioning Storage, USB Image Writer/RUFUS, BIOS/VM, and Verify Integrity
  If you want to dual-boot or boot more than a single OS, it is necessary and wise to partition the disk size to
at least the minimum recommended storage size, as well as a little more gigabytes (GB). I tried to experiment with
less space on a VM, and I found instability/slowdown/crashes resulted. 

  RUFUS is compatible with all OS, and the USB Image Writer app is integrated on Linux Mint. Both have the same
purpose of taking an OS image and translating the file for the USB to be bootable into the motherboard BIOS. 
It's always a good idea to check that the USB is formatted in a file type that works for the OS. I defaulted to
using NTFS [instead of FAT32] as it was fairly stable and up-to-date.

  We should always make sure the image quality or any downloads are safe. It's good practice to check sum, sha256,
and other text files to make sure the uploader is good. Otherwise, you can potentially be allowing a malicious
and insecure OS.

### Partitioning a disk on:
  Windows 11: 
1) (Search up w/ Windows key) Create and format a disk partition 
2) choose a disk
3) allocate disk size (rec. NTFS)
4) write an image on a USB to RUFUS
5) shut off the device
6) enter bios [F8, F12, etc.]
7) boot the desired image

  Linux Distributions: 
1) use the terminal/your preferred Graphical User Interface (GUI) to format disk to NTFS
2) choose a disk
3) allocate disk storage (rec. NTFS)
4) write an image on a USB w/ RUFUS, USB image writer, etc.
5) shut off the device
6) enter bios [F8, F12, etc.]
7) boot the desired image

You'll notice both are fairly similar, but with slightly different ways to get there.

NOTE:  Sometimes you might need to turn off Secure Boot for certain OS such as QubesOS or other distributions.
Hardware can conflict with certain OS, compatibility issues, etc. Usually older devices and/or AMD hardware
can be much more stable than NVIDIA due to open-source work from community members.
