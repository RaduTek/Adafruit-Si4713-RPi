# Python class for connecting to the Adafruit Si4713 (FM transmitter) breakout-board

Code reused from Adafruit's example code and Hansipete's original code. Converted into a reusable class by djazz/daniel-j. Uses Adafruit_I2C and RPi.GPIO, make sure those are available!

Original code is from this Adafruit forums thread:
https://forums.adafruit.com/viewtopic.php?f=50&t=58453

This file is included in this repo:
https://github.com/adafruit/Adafruit-Raspberry-Pi-Python-Code/blob/master/Adafruit_I2C/Adafruit_I2C.py

Don't forget to enable I2C! On current Raspberry Pi OS, run `sudo raspi-config` and enable the I2C interface.

## How to use

Connect the board's I2C pins to the Raspberry Pi I2C pins and the reset pin to GPIO4 (right next to the I2C/SPI pins). You can use 5V or 3V3 to power the board. Connect an audio source to the transmitter. Install the Python 3 dependencies first, then start the example with `sudo python3 radio.py`. Tune in to 101.0 MHz, and you should hear whatever audio you're inputting to the board. You should (if you have an RDS/RBDS supporting FM radio) see the station title too!

## Dependencies

On modern Raspberry Pi OS, install the packages needed by the driver:

```bash
sudo apt install python3-rpi.gpio python3-smbus
```

If your image does not provide `python3-smbus`, install `smbus2` instead:

```bash
python3 -m pip install smbus2
```

Happy pi-casting!