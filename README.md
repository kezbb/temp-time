# 温湿度传感器项目
## 概述

本项目演示如何使用 ESP8266 和 ESPHome 库创建一个类似于小米的温湿度传感器，并将其集成到 Home Assistant 中。

## 要求

- ESP8266或者ESP01/01S 板
- DHT11 或类似的温湿度传感器
- ESPHome 库
- Home Assistant

## 设置

1. **安装 ESPHome**：按照 [ESPHome 安装指南](https://esphome.io/guides/installing_esphome.html) 在您的计算机上设置 ESPHome。
2. **配置 ESPHome**：为您的 ESP8266 设备修改如下配置文件。替换为自己的2.4GWiFi名称和密码即可。

    ```yaml

    wifi:
      ssid: "your_SSID"
      password: "your_PASSWORD"

    ```

3. **上传配置**：将您的 ESP8266 连接到计算机，并使用 ESPHome 上传配置。

4. **与 Home Assistant 集成**：在 Home Assistant 中添加 ESPHome 集成，并配置其连接到您的 ESP8266 设备。

## 使用

设置完成后，您可以在 Home Assistant 中监控来自 ESP8266 传感器的温度和湿度读数，并在自动化中使用它们或在仪表板上显示它们。

## 参考资料

- [ESPHome 文档](https://esphome.io/)
- [Home Assistant 文档](https://www.home-assistant.io/docs/)
- [DHT22 传感器信息](https://learn.adafruit.com/dht)
