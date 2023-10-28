# AT-firmware-v2artifact

### AT firmware for esp8266 SoCs (ESP-WROOM-02D/02U) 1 MB version

This firmware is an ESP8266 Non-OS SDK that uses the *espconn* network interface and is not related to  ESP-AT (based on ESP-IDF or ESP8266_RTOS_SDK).

Reference documentation of AT-firmware v2.0.0.0 at [docs.espressif.com](https://espressif-docs.readthedocs-hosted.com/projects/esp-at/en/release-v2.2.0.0_esp8266/Get_Started/Hardware_connection.html#esp8266-series)

Source file at [github.com/espressif/ESP8266_NONOS_SDK/](https://github.com/espressif/ESP8266_NONOS_SDK/tree/master/bin/at#update-steps)

## Flash command

``esptool.py --trace write_flash @download.config``

## Flash config

This configuration is invoked when executed the flash command:

``--flash_mode dio --flash_freq 80m --flash_size 1MB 0x8000 partition_table/partition-table.bin 0x9000 ota_data_initial.bin 0x0 bootloader/bootloader.bin 0x20000 esp-at.bin 0x18000 at_customize.bin 0x1A000 customized_partitions/client_cert.bin 0x1B000 customized_partitions/client_key.bin 0x1C000 customized_partitions/client_ca.bin 0x1D000 customized_partitions/mqtt_cert.bin 0x1E000 customized_partitions/mqtt_key.bin 0x1F000 customized_partitions/mqtt_ca.bin 0x19000 customized_partitions/factory_param.bin``
