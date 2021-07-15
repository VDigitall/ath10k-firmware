# Fix problem with WI-FI adapter Qualcomm QCA6174 on Fedora 34

```shell
# Clone repo https://github.com/kvalo/ath10k-firmware.git
$ git clone https://github.com/kvalo/ath10k-firmware.git
$ cd ath10k-firmware

# Copy board-2.bin to /usr/lib/firmware/QCA6174/hw3.0/board-2.bin
$ cp QCA6174/hw3.0/board-2.bin /usr/lib/firmware/QCA6174/hw3.0/board-2.bin

# Copy latest firmware file (in my case)
$ cp QCA6174/hw3.0/4.4.1/firmware-6.bin_WLAN.RM.4.4.1-00282-QCARMSWPZ-1 /usr/lib/firmware/ath10k/QCA6174/hw3.0/firmware-6.bin

# Copy file board.bin which placed in this repo (file was taken from https://bugzilla.kernel.org/show_bug.cgi?id=108791#c2)
$ cp board.bin /usr/lib/firmware/ath10k/QCA6174/hw3.0/board.bin

# Reboot
$ reboot
```

Usefull links:
- https://askubuntu.com/questions/607707/ath10k-installation/718430
- https://bugzilla.kernel.org/show_bug.cgi?id=108791#c2
- https://bugzilla.kernel.org/attachment.cgi?id=196391
- https://github.com/kvalo/ath10k-firmware
