# Changelog

## 0.5.52
* improved ahoyWifi class
* added interface class for app
* refactored web and webApi -> RestApi
* fix calcSunrise was not called every day
* added MQTT RX counter to index.html
* all values are displayed on /live even if they are 0
* added MQTT <TOPIC>/status to show status over all inverters

## 0.5.51
* improved scheduler, @beegee3 #483
* refactored get NTP time, @beegee3 #483
* generate `bin.gz` only for 1M device ESP8285
* fix calcSunrise was not called every day
* incresed number of allowed characters for MQTT user, broker and password, @DanielR92
* added NRF24 info to Systeminfo, @DanielR92
* added timezone for monochrome displays, @gh-fx2
* added support for second inverter for monochrome displays, @gh-fx2

## 0.5.50
* fixed scheduler, uptime and timestamp counted too fast
* added / renamed automatically build outputs
* fixed MQTT ESP uptime on reconnect (not zero any more)
* changed uptime on index.html to count each second, synced with ESP each 10 seconds

## 0.5.49
* fixed AP mode on brand new ESP modules
* fixed `last_success` MQTT message
* fixed MQTT inverter available status at sunset
* reordered enqueue commands after boot up to prevent same payload length for successive commands
* added automatic build for Nokia5110 and SSD1306 displays (ESP8266)

## 0.5.48
* added MQTT message send at sunset
* added monochrome display support
* added `once` and `onceAt` to scheduler to make code cleaner
* improved sunrise / sunset calculation

## 0.5.47
* refactored ahoyWifi class: AP is opened on every boot, once station connection is successful the AP will be closed
* improved NTP sync after boot, faster sync
* fix NRF24 details only on valid SPI connection

## 0.5.46
* fix sunrise / sunset calculation
* improved setup.html: `reboot on save` is checked as default

## 0.5.45
* changed MQTT last will topic from `status` to `mqtt`
* fix sunrise / sunset calculation
* fix time of serial web console

## 0.5.44
* marked some MQTT messages as retained
* moved global functions to global location (no duplicates)
* changed index.html inverval to static 10 seconds
* fix static IP
* fix NTP with static IP
* print MQTT info only if MQTT was configured

## 0.5.43
* updated REST API and MQTT (both of them use the same functionality)
* added ESP-heap information as MQTT message
* changed output name of automatic development build to fixed name (to have a static link from https://ahoydtu.de)
* updated user manual to latest MQTT and API changes

## 0.5.42
* fix web logout (auto logout)
* switched MQTT library