# ping.py

Ping is a python program that runs on a raspberry pi to restart a router using a relay and log internet outages. 


## Installation

Clone the repository in to your home folder on a Raspberry Pi

Add ping.py to startup

Connect the relay to the Raspberry Pi on pin 12 (GPIO 18), ground (GND) and 5V DC power. These pins can be changed in the code if needed.

![Pinnout](https://linuxhint.com/wp-content/uploads/2022/02/image6-34.png)
Source: [https://linuxhint.com/wp-content/uploads/2022/02/image6-34.png](https://linuxhint.com/wp-content/uploads/2022/02/image6-34.png)

## Bash scripts (optional)

These scrips are for looking at logs. Place the in your home folder. 
Make the script exicutable with:
```shell
sudo chmod +x <filename>
```

Run by using: `./filename.sh`

logs.sh looks at the log file and prints it to the terminal using `less`. 
```shell
#! /bin/sh
less ping/Logs.txt
```

tlog.sh automatically updates the log in real time. 
```shell
#! /bin/sh
tail -f ping/Logs.txt
```
