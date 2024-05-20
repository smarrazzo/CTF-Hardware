# Flash CTF on ESP32

esptool --chip esp32 --port "COM13" --baud 921600  --before default_reset --after hard_reset write_flash  -z --flash_mode dio --flash_freq 80m --flash_size 4MB 0x1000 CTF_ESP32.ino.bootloader.bin 0x8000 CTF_ESP32.ino.partitions.bin 0xe000 boot_app0.bin 0x10000 CTF_ESP32.ino.bin