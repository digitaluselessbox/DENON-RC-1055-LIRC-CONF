# DENON-RC-1055-LIRC-CONF

While I was playing around with my Raspberry Pi and some IR-Receiver and IR-Transmitter I did a IR configuration of my Denon 1055 remote controll.

Actually my first test was a very special situation, because this rc has two different "ir-profiles" in it. It take me a while to fire out why sometimes everything works ans why not. Basically you can not mix two different ir signales in one configuration. The configuration includes many stuff that is neseccarry for the ir signal like gaps, header, bits, ect... I did not go in detail for all the different configurations. ;) 

What i did was to create two configuration files. One file for each package of keys. On the remote you can see the number block that is souround by a line. This block has a different ir signal than all the other keys. Maybe this is to controll other Denon devices like CD-Players or something like that.

## Raspberry Configuration

### Hardware

- Raspberry Pi 3 Model B Rev 1.2
- AZ-Delivery KY-022 ir-receiver
- AZ-Delivery KY-005 ir-transmitter
- DENON RC-1055 using to controll DRA-500AE HiFi-Receiver

### Software

- Raspbian GNU/Linux 10 (buster)
    - Linux raspberrypi 5.4.83-v7+
- lircd 0.10.1

