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

