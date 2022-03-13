# Overview
This project contains part of my smarthome implementation.
As image [Max2Play](https://www.max2play.com/en/getting-started/) is used. For this reason not the entire setup is documented. This reposotory contains a backup of the RaspBee configuration, as well as the openhab configuration. 
The main features are an alarm clock, which turns on the spearker before the android alarm clock rings, access to all Zigbee devices with Openhab, radio control of the squeezebox server [select radio stations, if in favorites] and spotify connect.

# Hardware
- RaspberryPi 3
- [HifiBerry AMP 2](https://www.hifiberry.com/shop/boards/hifiberry-amp2/)
- [RaspBee Zigbee gateway](https://phoscon.de/en/raspbee)
# Zigbee devices
- [OSRAM Smart+ Plug, Zigbee](https://www.amazon.de/-/en/gp/product/B074PZLX2P/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)
- [OSRAM Smart+ LED, Zigbee](https://www.amazon.de/-/en/gp/product/B074KJ72MP/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)
- [OSRAM Smart+ LED Stripe, Zigbee](https://www.amazon.de/-/en/gp/product/B07482ZJLY/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)
- [Aquara Smart Air Pressure, Temperature, Humidity and Ambient Sensor](https://www.amazon.de/-/en/gp/product/B07R9VCQ5N/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)
- Philips Hue White Ambiance Deckenleuchte Being aluminium

# Getting started
Download and configure [Max2Play](https://www.max2play.com/en/getting-started/), install squeezebox server and plugins (spotty)
Install [deconz](https://phoscon.de/en/raspbee/install#raspbian), set to HTTP pport 81:
- `sudo systemctl nano deconz`
- Set ExecStart to: `ExecStart=/usr/bin/deCONZ -platform minimal --http-port=81`
Install [openhab](https://www.openhab.org/docs/installation/linux.html#installation)
Clone repository into /etc/openhab, import Backup into phoscon app.