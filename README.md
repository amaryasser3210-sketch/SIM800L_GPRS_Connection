**SIM800L Firmware update**
The problem was with the https request encryption the SIM800L firmware is connected using the Tinygsm client which is the responsable for creating the https request with TSL1.0 encryption, TSL1.0 is quit old version. These days TSL1.3 is a standard in backends communications.
For SUPABASE requires at least TSL1.2. <br>
<br>
Our current module firmware version is **1418B05SIM800L24** which is the latest version i found online. <br>
But next I found **1418B06SIM800L24** on [github repostry](https://github.com/Ircama/sim800l-gsm-module/blob/master/firmware/README.md) from a non-verified source. The repostry owner says when he tested the latest TSL version supported by SIM800L it was TSL1.0.

You can find the firmware uploader software in [here](https://simcom.ee/documents/?dir=) and more in mentioned repostry ubove.<br>
<img width="640" height="420" alt="image" src="https://github.com/user-attachments/assets/bfe917b1-8e18-488a-ad4e-d9c2c24a3a2a" /> <br>
<br>
_circuit for SIM800 firmware update through UART to USB_ 

**Protocol Gateway**
There is another solution which is Reverse Proxy (gatewaying) through a web server using NGINX. 
.
.
.
