## Zigbee Button

### Getting started

#### Prerequisites

TB-03F module from AiThinker

#### Write programmer (Linux)

1. connect the SWS pin to pin 2 of CH340 of the TB-03F
   ![TB-03F](image/TB-03F.png)
2. connect TB-03F to computer and find which port the TB-03F is connected to with `ls /dev/tty*` (mine is `/dev/ttyUSB1`)
3. go to programmer-directory and run `python TlsrComProg.py -p <port> -t5000 we 0 uart2swire.bin` with raplecing `<port>` with the port of the TB-03F found in previous step
4. 
5. 
6. output:

```
python3 TlsrComProg.py -p /dev/ttyUSB1  rf 0 0x10000 d.bin
```

```
================================================
TLSR825x Floader version 27.12.23
------------------------------------------------
Open /dev/ttyUSB1, 230400 baud...
Reset module (RTS low)...
Activate (600 ms)...
Warning: Wrong RX-TX connection?
Connection...
Load <floader.bin> to 0x40000...
Bin bytes writen: 1960
CPU go Start...
------------------------------------------------
ChipID: 0x5562 (TLSR8253), Floader ver: 1.1
Flash JEDEC ID: c86013, Size: 512 kbytes
------------------------------------------------
Read Flash from 0x000000 to 0x010000...
Outfile: d.bin
------------------------------------------------
(1) Warning
```

Credits to [TLSRPGM](https://github.com/pvvx/TLSRPGM)

#### Flashing

1. connect ZT3L to TB-03F
   ![ZT3L](image/ZT3L.png)
   ![TB-03F_1](image/TB-03F_1.png)
   SWS     <-->    SWM
   +3.3V  <-->    +3.3V
   GND     <-->    GND

##### Test connection

Running `python TlsrPgm.py -s -p <port> i` should give you give you an output like this:

Troubleshooting

- **Error get Chip ID! (102)**

Credits to [tuyaZigbee](https://github.com/doctor64/tuyaZigbee)
