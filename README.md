# Documents

Here you can find all basic document for this project

FAQ for quick start:

I. GATEWAY

1. Did you register an account in (http://www.i4things.com/) ?
2. Did you register a gateway in (http://www.i4things.com/) members area ?
3. Did you set the SSID and PASS ( your local wifi credential) to the gateway using the Gateway Configurator ?
4. Did you set gateway Key, Gateway ID and frequency using Gateway Configuratior ?
5. Did you Gateway shows on the LED screen wifi connection strength  > 0% ? e.g. have connection ?
6. Did you check in the (http://www.i4things.com/) Members Area - click over the gateway and inside you have chart with updates from the gateway - that you gateway is sending heartbeats ? ( the temperature and humidity is expected to show -20 and Humidity 0% if you do not have sensor connected )

II. NODE

1. Did you choose hardware ? ESP32(Heltec or TTGO ) or AVR/Feather ?
2. Did you register a Node in (http://www.i4things.com/) members area ?
3. Did you choose a example for your Node ?

e.g.  like this one :

https://github.com/i4things/NodeAPI/tree/master/examples/ESP32/HELTEC/Simple/thing

Node/Device API for sending and receiving data over LoRa or WiFi/Ethernet - i4things/NodeAPI

4. When open it in arduino IDE - select board Heltec 

(
FOR 433 or 915 MHZ ONLY !!!!  in the file IoTThing.h line : 882
change it to : float all_freq[IoTThing_FREQ_CNT] = { 433.0f , 443.0f, 433.0f };
)

5. Next in the file thing.ino - line 31 you need to set the id to be the one that you got when created a node in www.i4things,com
6. run the example and what the screen of the gateway - do you see the counters ( the one with numbers) to increase ? -f YES the Lora Communication is good. 

7. Go in (http://www.i4things.com/) members area and click on the node - do you see any data in the chart ? if yes - all is good with the communication till the server

8. Open with editor the file : iot_get.html

and on line : 94 and 95 fill the ID and Network Key of the node that you got when created a node in (http://www.i4things.com/)

9. Open the html in a browser ( e.g. Chrome ) do you see data from the node ? if YES - all is perfect and you can continue to implement your ideas inside the node example in Arduino IDE and read this data like in the example HTML - also please read the short docs in github and www.i4things.com 
