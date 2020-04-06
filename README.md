# ## onion-omega2-openwrt ##
Install openwrt on onion omega2+ for STA only mode

# Power Dock 2 - connect serial port of Onion Omega2+
If you are like me, you purchased a PowerDock 2 and for some reason, the manufacturer decided not to include Serial0 on thier fancy breakout header.  Would have been nice if they designed the pins to fit into a standard size breadboard like many other dev boards...

So I decided to just solder on a couple of wires to the RX0 TX0 pins on the PowerDock 2 so that I can use my own 3v3 USB-SERIAL converter.

<img src="pictures/solder-serial-powerdock2.jpg" alt="Picture of Serial Solder Connections" style="float: left; margin-right: 10px;" />

Next, complete the TX, RX and GND Connections (remember RX-TX TX-RX).  Bring up a terminal on the correct COM port with settings of 115200 8,N,1,N.

Power on the device and the boot up sequence should show up in the terminal
<img src="pictures/serial_powerdock2.jpg" alt="Picture of Serial Connections" style="float: left; margin-right: 10px;" />
