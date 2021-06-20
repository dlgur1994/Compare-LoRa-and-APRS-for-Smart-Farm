# Compare LoRa and APRS for Smart Farm

## 1. About
- Compare LoRa and APRS to find out an adequate network for monitoring a orchard for a farmer who lives 30 miles away.

## 2. Environment
- LoRa: Arduino Uno, Arduino LoRa/GPS Shield v1.4, wlaniot 900MHz Antenna, 824-960 MHz 6 dBi 900MHz Omni Antenna
- APRS: Arduino Uno, Radiometrix HX1-144.390-3, USRP b200 USB Software Defined Radio, Nagoya UT-72 Antenna, X2200A Dualband Base/Repeater Antenna
> |Specifications|LoRa|APRS|
> |---|---|---|
> |Transmitted Power|16 dBm|24 dBm|
> |Transmitter Antenna Gain|9 dBi|1.17 dBi|
> |Receiver Antenna Gain|6 dBi|6 dBi|
> |Theoretical Distance|9.3 km|59.7 km|
> |Fresnel Zone Radius|27.79 m|176.02 m|
> |60% of Fresnel Zone Radius|16.67 m| 105.61 m|

## 3. Installation
- GNU Radio for APRS<br/>
    - https://wiki.gnuradio.org/index.php/InstallingGR

## 4. Code

## 5. Result
- LoRa is more feasible than APRS for the networking technology in smart farms without considerable investments in towers and/or repeaters.<br/>
> |Network|Distance|Efficiency constrained by Height|
> |---|---|---|
> |**LoRa**|**4.2km**|**45.16%**|
> |APRS|0.84km|1.44%|