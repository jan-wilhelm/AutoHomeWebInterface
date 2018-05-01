# AutoHomeWebInterface

![](https://hu11a.dynvpn.de/android-icon-192x192.png)
> The project&apos;s logo (5 minutes in Photoshop)

This is the website and Rest API for my AutoHome project.
## How it started
I started this project when I was 15 years old and for the first time actively realized that our *magic* remote controlled electrical outlets are actually remote controlled and therefore can also be controlled by any kind of radio transmitter. Without a bigger project in mind, my dad had given me a Raspberry PI 3 for my birthday a few months earlier. A few quick google searches later and I found what I looked for: A [433mHz transmitter for the RasPi](https://www.amazon.com/UCEC-XY-MK-5V-Transmitter-Receiver-Raspberry/dp/B017AYH5G0/ref=sr_1_fkmr0_1?ie=UTF8&qid=1525002346&sr=8-1-fkmr0&keywords=433mhz+transmitter+raspi) and a pack of [120 breadboard wires](https://www.amazon.com/Elegoo-EL-CP-004-Multicolored-Breadboard-arduino/dp/B01EV70C78/ref=sr_1_3?ie=UTF8&qid=1525002402&sr=8-3&keywords=elegoo+wires).

## Libraries I use

+ **For the website**
    * [Composer](https://getcomposer.org/)
    * [KLogger](https://github.com/katzgrau/KLogger)
    * The [Philips Hue API](https://www.developers.meethue.com/philips-hue-api)

+ **For the app**
    * The [MapBox Maps API](https://www.mapbox.com/api-documentation/#maps)

+ **For the voice platform**
    * [Snips](https://snips.ai) (an incredible, free Voice-Recognition and NLU platform)
    * [Requests](http://docs.python-requests.org/en/master/)
    * [JSON parsing library](https://docs.python.org/3/library/json.html)
    * [MQTT Python library](https://pypi.org/project/paho-mqtt/)

## The system design
![](https://i.imgur.com/9Q0yUle.png)
This is a pretty simplified scheme of how I designed my project.
The leftmost layer is the user&apos;s input, either via voice, through the app or on the website. The master server runs the website and the API on a Synology Diskstation. It also manages the MySQL database and the routine service.

**Note:** This is the first commit of the project description. More to come.
