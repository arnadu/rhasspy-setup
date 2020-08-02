# rhasspy-setup

home assistant to control sonos and tv, etc...
in replacement of the SNIPS setup

hardware
--------

raspberry pi 3
respeaker 4 mic array

raspberry config
----------------

hostname=snips
ip=192.168.1.31

** Install respeaker driver
use option compat-kernel when running install.sh: 
--sudo ./install.sh --compat-kernel
https://wiki.seeedstudio.com/ReSpeaker_4_Mic_Array_for_Raspberry_Pi/

** Install the MQTT broker: mosquitto
https://randomnerdtutorials.com/how-to-install-mosquitto-broker-on-raspberry-pi/
sudo apt install -y mosquitto mosquitto-clients
sudo systemctl enable mosquitto.service
mosquitto_sub -d -t testTopic
mosquitto_pub -d -t testTopic -m "Hello"

** Install docker (instructions from rhasspy install tutorial)
curl -sSL https://get.docker.com | shcurl -sSL https://get.docker.com | sh
sudo usermod -a -G docker $USER


** Install rhasspy through docker

https://rhasspy.readthedocs.io/en/latest/installation/

** Install LED control
https://github.com/project-alice-assistant/HermesLedControl/wiki/Installation-&-update


