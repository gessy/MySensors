MySensors Library v2.3.0-alpha

It has been tested on the Orange Pi Zero 512MB platform (OS ARMBIAN 5.35 Debian GNU/Linux 8 (jessie) 3.4.113-sun8i) and Semtech SX1278 radio (RA-02 module)

Default settings
----------------

- Working frequency: 433.9 MHz
- BW: 125 kHz
- CR: 4/5
- SF: 128
- Tx power: 13 dBm (20 mW)
- ATC mode disabled

Connections
-----------
- SX1278 - Orange Pi Zero

- 3.3V   - 3.3V (header pin #17) 
- GND	   - GND (pin #25)
- MOSI   - MOSI (pin #19)
- MISO   - MISO (pin #21)
- SCK    - CLK (pin #23)
- DIO0   - GPIO2 (pin #22)
- NSS    - GPIO13 (pin #24)

Download
--------
```
git clone https://github.com/vladikoms/MySensors.git
cd MySensors
```

Optional settings
-----------------

If you need other frequency, power, modem configuration, etc.. please edit RFM95 section in MyConfig.h file

Configurate
-----------

``
./configure --spi-spidev-device=/dev/spidev1.0 --my-transport=rfm95 --my-gateway=ethernet --my-port=5003
``

Compile
-------
```
make
```

Test Run
------
```
sudo ./bin/mysgw
```

Install
-----

```
sudo make install
```

To start service automatically when the Orange Pie boots:

```
sudo systemctl enable mysgw.service
```

More information
-----
Please visit www.mysensors.org
