# DENON-RC-1055-LIRC-CONF

While I was playing around with my Raspberry Pi and some IR-Receiver and IR-Transmitter I did a IR configuration of my Denon 1055 remote controll.

Actually my first test was a very special situation. It take me a while to find out why sometimes everything works ans why not.


## Raspberry Configuration

### Hardware

- Raspberry Pi 3 Model B Rev 1.2
- AZ-Delivery KY-022 ir-receiver
- AZ-Delivery KY-005 ir-transmitter

### Software

- Raspbian GNU/Linux 10 (buster)
    - Linux raspberrypi 5.4.83-v7+
- lircd 0.10.1

## Remote Control

**Brand:** Denon  
**Model:** RC-1055  
**Used for device:** DRA-500AE  
**Used for device type:** HiFi-Receiver  

This rc has two different "ir-profiles" in it. The problem i, you can not mix two different ir signales in one configuration. The configuration includes many stuff that is neseccarry for the ir signal like gaps, header, bits, ect... I did not go in detail for all the different configurations. ;) 

So I created two configuration files. One file for each "ir-profile". On the remote you can see the number block that is souround by a line. This block has a different ir signal than all the other keys. Maybe this is to controll other Denon devices like CD-Players or something like that. I put this keys in **Profile 2**. In **Profile 1** I inluded all main Keys like Power or Volume. 

### Profile 1 Keys:

**Key:** OFF, ON, CD, DVD, TUNER, CD-R/TAPE-1, MD/TAPE-2, AUX, PREVIOUS CHANNEL, NEXT CHANNEL, VOLUME UP, VOLUME DOWN, MUTE, SHIFT/PTY, MENU, UP, RDS, LEFT, ENTER, RIGHT, BAND, STATUS, DOWN, IPOD

**Filename:** DENON_1055_1.lircd.conf

### Profile 2 keys:

**Keys:** 1, 2, 3, 4, 5, 6, 7, 8, 9, 0, +10, SKIP/DISK, PLAY, PAUSE, STOP, PREV, NEXT

**Filename:** DENON_1055_2.lircd.conf

