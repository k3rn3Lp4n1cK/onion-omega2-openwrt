# onion-omega2-openwrt
Install openwrt on onion omega2+ for STA only mode

# Power Dock 2 - connect serial port of Onion Omega2+
If you are like me, you purchased a PowerDock 2 and for some reason, the manufacturer decided not to include Serial0 on thier fancy breakout header.  Would have been nice if they designed the pins to fit into a standard size breadboard like many other dev boards...

So I decided to just solder on a couple of wires to the RX0 TX0 pins on the PowerDock 2 so that I can use my own 3v3 USB-TTY converter.

<img src="pictures/solder-serial-powerdock2.jpg" alt="Picture of Serial Solder Connections" style="float: left; margin-right: 10px;" />

Next, complete the TX, RX and GND Connections (remember RX-TX TX-RX).  Bring up a terminal on the correct COM port with settings of 115200 8,N,1,N.

Power on the device and the boot up sequence should show up in the terminal
<img src="pictures/serial_powerdock2.jpg" alt="Picture of Serial Connections" style="float: left; margin-right: 10px;" />

# Install OpenWRT Firmware on Onion Omega2+
Download the latest openwrt firmware from https://openwrt.org/toh/hwdata/onion/onion_omega2plus

The latest edition at the time of this document was openwrt version 19.07.2.

scp or wget the openwrt firmware to the Omega2+ and execute a sysupgrade.

```
cd /tmp
wget http://downloads.openwrt.org/snapshots/targets/ramips/mt76x8/openwrt-ramips-mt76x8-onion_omega2p-squashfs-sysupgrade.bin
sysupgrade /tmp/openwrt-ramips-mt76x8-onion_omega2p-squashfs-sysupgrade.bin
```

The Omega2+ will reboot.  Once reboot is complete, an open openwrt wireless access point will be available for connection.

*note: My setup would not reboot if my usb-tty converter was connected. I had to remove all power from Omega2+ Power Dock 2 and pull the USB-TTY device from the usb port.  I would then power on the Omega, plug in the USB-TTY device and open a serial console port in a terminal in that exact order.

