# ESP8266_DNS_sinkhole
A DNS sinkhole to block ads on your network. Using a ESP8266 microcontroller.


sinkhole:

0. Edit SSID and password in the code. Add websites to the blacklist[] as you see fit.
1. Push the code to your ESP8266 using Arduino IDE.
2. Go to your router and figure out the IP to your ESP
3. Set the ESP IP as static ip
4. Set the DNS on your device to the static ip you set.
5. Go to http://theIPyouSet/logs to see the logs on what's going on.



sinkhole_OLED_dynamicBlacklist

Made for: ESP8266 Development Board With 2.44 Cm OLED Display, CH340 Driver, ESP-12E WiFi Wireless Module, And Micro USB Works Great For Arduino IDE/Micropython Programming (Pin Header Soldered)

0. Edit SSID and password in the code. Add websites to the blacklist[] as you see fit.
1. Change the dynamic blacklist URL if you want to, for a custom list you can update from your computer. Current: hostformat=hosts&showintro=1&startday=31&startmonth=08&startyear=2023&mimetype=plaintext&useip=none
   - Make sure that the list you choose is formatted exactly the same way, if you dont want to change the code. And be sure its not too big, as the memory of the ESP8266 is limited ( 128KB )
3. Push the code to your ESP8266 using Arduino IDE.
4. Go to your router and figure out the IP to your ESP
5. Set the ESP IP as static ip
6. Set the DNS on your device to the static ip you set.
7. Go to http://theIPyouSet/ to see whats going on. You can click on "View Logs" or "update blacklist".
8. The blacklist will automatically update itself using the provided URL every 24 hours, but can also be imidiatly updated using "update blacklist" button @ http://theIPyouSet/
