# ESP32 Deauther

(Maybe) Port of https://github.com/spacehuhn/esp8266_deauther to the ESP32,
based on the `esp_wifi_80211_tx` function described in https://github.com/Jeija/esp32-80211-tx

# Building

`idf.py build`

Built with v4.1-dev-763-ga45e99853

# Flashing

**IMPORTANT IF YOU WANT TO DEAUTH:** Due to a deauth lock implemented by espressif, the
ELF file generated by `idf.py build` must be patched to allow sending deauth packets. To
do that, run `./patch.sh build/deauther.elf` between building and flashing.

`idf.py flash`

