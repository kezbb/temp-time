# temp-time
## Overview

This project demonstrates how to use an ESP8266 with the ESPHome library to create a temperature and humidity sensor similar to Xiaomi's, which can be integrated into Home Assistant.

## Requirements

- ESP8266 board
- DHT22 or similar temperature and humidity sensor
- ESPHome library
- Home Assistant

## Setup

1. **Install ESPHome**: Follow the [ESPHome installation guide](https://esphome.io/guides/installing_esphome.html) to set up ESPHome on your computer.
2. **Configure ESPHome**: Create a new configuration file for your ESP8266 device. Below is an example configuration:

    ```yaml
    esphome:
      name: temp_time_sensor
      platform: ESP8266
      board: nodemcuv2

    wifi:
      ssid: "your_SSID"
      password: "your_PASSWORD"

    sensor:
      - platform: dht
        pin: D2
        temperature:
          name: "Living Room Temperature"
        humidity:
          name: "Living Room Humidity"
        update_interval: 60s

    logger:

    api:

    ota:
    ```

3. **Upload Configuration**: Connect your ESP8266 to your computer and upload the configuration using ESPHome.

4. **Integrate with Home Assistant**: Add the ESPHome integration in Home Assistant and configure it to connect to your ESP8266 device.

## Usage

Once set up, you can monitor the temperature and humidity readings from your ESP8266 sensor in Home Assistant, and use them in automations or display them on your dashboard.

## References

- [ESPHome Documentation](https://esphome.io/)
- [Home Assistant Documentation](https://www.home-assistant.io/docs/)
- [DHT22 Sensor Information](https://learn.adafruit.com/dht)
