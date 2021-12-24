# Simple clone of wiringPi's 'gpio readall'

Since wiringPi is no longer developed (see http://wiringpi.com/news)
and is not contained in Raspberry Pi OS version Bullseye any more
the command 'gpio' is gone.

And so the really helpfull 'gpio readall' too.

This simple Python script here aims to give a similar output.

    state mode BCM  name   Physical name   BCM mode state
    -----------------------------------------------------
                     3.3V   1 |  2  5V
      1    in   2   SDA.1   3 |  4  5V
      1    in   3   SCL.1   5 |  6  GND
      1    in   4           7 |  8  TxD     14  in     1
                      GND   9 | 10  RxD     15  in     1
      0    in  17          11 | 12          18  in     0
      0    in  27          13 | 14  GND
      0    in  22          15 | 16          23  in     0
                     3.3V  17 | 18          24  in     0
      0    in  10    MOSI  19 | 20  GND
      0    in   9    MISO  21 | 22          25  in     0
      0    in  11    SCLK  23 | 24  CE0      8  in     1
                      GND  25 | 26  CE1      7  in     1
      1    in   0   SDA.0  27 | 28  SCL.0    1  in     1
      1    in   5          29 | 30  GND
      1    in   6          31 | 32          12  in     0
      0    in  13          33 | 34  GND
      0    in  19          35 | 36          16  in     0
      0    in  26          37 | 38          20  in     0
                      GND  39 | 40          21  in     0

It has been tested with a Raspberry Pi version 2B and a Pi400 yet.

The program uses *pigpio*. To make it work the daemon *pigpiod* needs to be running!

Start it once with:

    sudo pigpiod

or for automatic start on every boot:

    sudo systemctl enable --now pigpiod


No warranties at all - as usual.

Comments and suggestions are welcome.
