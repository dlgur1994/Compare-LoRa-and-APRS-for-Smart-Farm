# Compare LoRa and APRS for Smart Farm

## 1. About
- This project compared LoRa and APRS to a suitable network for monitoring farmers' orchards 30 miles away. It was conducted with support from IITP, a Korean government agency, and Purdue University in the United States.

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
- GNU Radio for APRS(need USRP b200 USB Software Defined Radio)<br/>
    - https://wiki.gnuradio.org/index.php/InstallingGR

## 4. Code
- LoRa<br/>
    - Transmitter: LoRa/LoRa_Transmitt.ino
    - Receiver: LoRa/LoRa_Reciever.ino
- APRS<br/>
    - Transmitter: APRS/Transmitter/APRS_Transmitter.ino 
    - Receiver: APRS/APRS_Receiver.py

## 5. Result
- Expecting networking distances were calculated by the Friis Transmission formula. However, because APRS was more affected by the Fresnel Zone than LoRa, the actual network communication distance of APRS at a lower height was shorter than expected. **So, LoRa was more feasible than APRS for the networking technology in smart farms** without considerable investments in towers and/or repeaters.<br/>
> |Network|Coverage Distance|Efficiency constrained by Height|
> |---|---|---|
> |**LoRa**|**4.2km**|**45.16%**|
> |APRS|0.84km|1.44%|

## 6. Publication
- 2020 IEEE International Conference on Omni-layer Intelligent Systems (COINS), Barcelona, Spain (Virtual)
- https://github.com/dlgur1994/Comparing-LoRa-and-APRS-for-Smart-Farm/blob/main/Publication/Feasibility%20of%20Networking%20Technology%20for%20Smart%20Farm-%20LoRa%20vs%20APRS.pdf