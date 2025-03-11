# Backup und Installation

`pigpio` kann man nach dem Neustart auch mit `sudo apt install pigpio`installieren laut ChatGPT.
Das Backup hier fasst alles zusammen, was in dem Ordner pigpio-master lag.

mavlink und px4 müssen sichergestllt werden, dass sie mit ROS 2 jazzy kompatibel sind. Hier ist ein backup von dem mavlink-router Ordner und der .px4 firmware Datei.

Laut CHatGPT kann Px4 neuaufgesetzt werden, indem man:
```bash
git clone --recursive https://github.com/PX4/PX4-Autopilot.git
cd PX4-Autopilot
bash Tools/setup/ubuntu.sh
```
##`bin`
### `px_uploader.py` – PX4 Firmware Uploader
- ein Skript, das oft mit PX4 verwendet wird, um Firmware auf einen PX4-Controller zu flashen
- es könnte aus der Px$-Installation (PX4-Autopilot/Tools/) kommen
Falls es nach der Neuinstallation nicht hinzugefügt wird, kann man es aus dem bin backup widerherstellen
### `teensy_loader_cli` – Firmware-Upload für Teensy
Dieses Tool wird genutzt, um Firmware auf einen Teensy-Mikrocontroller hochzuladen.
Dieses kam nicht aus einem `apt`-Paket, daher muss es bei der Neuinstallation auch sehr wahrscheinlich aus dem backup widerhergestellt werden

## `firmware.hex` - Mikrocontroller Firmware
- ist eine kompilierte Firmware-Datei für einen Mikrocontroller

`file firmware.hex` ergab:           
firmware.hex: ASCII text, with CRLF line terminators

- Falls es PX4 ist, kannst du eine neue .hex-Datei generieren.
- Falls es für Teensy ist, kannst du sie mit `teensy_loader_cli` wieder flashen.
