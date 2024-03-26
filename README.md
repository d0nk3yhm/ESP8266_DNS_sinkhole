# ESP8266_DNS_sinkhole
A DNS sinkhole to block ads on your network. Using a ESP8266 microcontroller.

0. Edit username and password in the code. Add blocked websites to the blacklist[] as you see fit.
1. Push the code to your ESP8266 using Arduino IDE.
2. Go to your router and figure out the IP to your ESP
3. Set the ESP IP as static ip
4. Set the DNS on your device to the static ip you set.
5. Go to http://theIPyouSet/logs to see the logs on what's going on.
