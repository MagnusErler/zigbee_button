## Zigbee Button

### Flashing

##### Prerequisites

TB-03F module from AiThinker

##### Write programmer (Linux)

1. connect the SWS pin to pin 2 of CH340
![TB-03F](image/TB-03F.png)
2. connect board to computer and find port with `ls /dev/tty*` (mine is `/dev/ttyUSB1`)
3. go to programmer-directory and run `python TlsrComProg.py -p <port> -t5000 we 0 uart2swire.bin` with raplecing `<port>` with the port of the TB-03F

Credits to [TLSRPGM](https://github.com/pvvx/TLSRPGM)

Credits to [tuyaZigbee](https://github.com/doctor64/tuyaZigbee)
