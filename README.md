# WarBerryPi 
![alt tag](https://github.com/secgroundzero/warberry/blob/master/SCREENS/Warberry_Logo_Transparent.png)

![GPLv3 License](https://img.shields.io/badge/License-GPLv3-red.svg)
[![Python 2.6|2.7](https://img.shields.io/badge/python-2.6|2.7-yellow.svg)](https://www.python.org/)
[![Twitter](https://img.shields.io/badge/twitter-@sec_groundzero-blue.svg)](https://twitter.com/sec_groundzero)


The **WarBerry** was built with one goal in mind; to be used in red teaming engagement where we want to obtain as much information 
as possible in a short period of time with being as stealth as possible. 
Just find a network port and plug it in. The scripts have been designed in a way that the approach is targeted to avoid noise 
in the network that could lead to detection and to be as efficient as possible. 
The WarBerry script is a collection of scanning tools put together to provide that functionality.



####Disclaimer
This tool is only for academic purposes and testing  under controlled environments. Do not use without obtaining proper authorization
from the network owner of the network under testing.
The author bears no responsibility for any misuse of the tool.


####Usage

To get a list of all options and switches use:

```python warberry.py -h```

```

Options:

  --version                             show program's version number and exit
  -h, --help                            show this help message and exit
  -a ATTACKTYPE, --attack=ATTACKTYPE    Attack Mode. Default: --attack
  -p PACKETS, --packets=PACKETS         Number of Network Packets to capture
  -I IFACE, --interface=IFACE           Network Interface to use. Default: eth0
  -N NAME, --name=NAME                  Hostname to use. Default: Auto
  -i INTENSITY, --intensity=INTENSITY   Port scan intensity. Default: T4
  -P, --poison                          Turn Poisoning on/off. Default: On
  -H, --hostname                        Do not Change WarBerry hostname Default: Off
  -e, --enumeration                     Disable Enumeration mode. Default: Off
  -M, --malicious                       Enable Malicious only mode Default: Off
  -r, --recon                           Enable Recon only mode. Default: Off
  -S, --sniffer                         Enable Sniffer only mode. Default: Off
  -C, --clear                           Clear previous output folders in ../Results
  -m, --man                             Print WarBerry man pages


example usage: sudo python warberry.py -a -T                Attack all TCP Ports
               sudo python warberry.py --attack --toptcp    Scan only the top udp ports
               sudo python warberry.py -r                   Use only the recon modules
               sudo python warberry.py -H -I wlan0          Use the wlan0 interface and dont change hostname
               sudo python warberry.py -I eth0 -i -T3       Use the eth0 interface and T3 scanning intensity
               sudo python warberry.py -I eth0 -N HackerPC  Use the eth0 interface and change hostname to HackerPC

```


### Installation

Detailed installation steps can be found at '**[usage](https://github.com/secgroundzero/warberry/wiki/installation)**' wiki page.



### Reporting 
Download the /WarBerry/RESULTS folder into the REPORTING/RESULTS folder and open reporting.html.
Apache is needed for the reporting tool to work. In Windows download XAMMP and install Apache.


### Important

The tool in case of MAC address filtering enumerates by default the subnets specified under ***/home/pi/WarBerry/warberry/discover***.
This is done for the tool to run quicker.
If you want to enumerate more subnets either add the subnets in that file or change line 154 in rest_bypass.py so that it does not
read from the file.


### Running Status

If you are connecting through SSH you can check the status of the attacks by checking the results_status file under Results. The file gets
updated after each phase is completed.


#### Dependencies

- sudo apt-get install nbtscan 
- sudo apt-get install python-scapy 
- sudo apt-get install tcpdump 
- sudo apt-get install nmap 
- sudo pip install python-nmap 
- sudo apt-get install python-bluez
- sudo pip install optparse-pretty
- sudo pip install netaddr
- sudo pip install ipaddress 
- sudo apt-get install ppp 
- sudo apt-get install xprobe2
- sudo apt-get install sg3-utils 
- sudo apt-get install netdiscover 
- sudo apt-get install macchanger 
- sudo wget http://seclists.org/nmap-dev/2016/q2/att-201/clamav-exec.nse  /usr/share/nmap/scripts/
- sudo git clone https://github.com/DanMcInerney/net-creds.git #install in /home/pi/WarBerry/Tools/


#### Extra Tools for Post Exploitation. Best to install in /home/pi/WarBerry/Tools/ directory

- sudo apt-get install onesixtyone
- sudo apt-get install nikto
- sudo apt-get install hydra
- sudo apt-get install john
- sudo apt-get install bridge-utils
- sudo apt-get install w3af-console
- sudo apt-get install ettercap-text-only
- sudo apt-get install cryptcat
- sudo apt-get install ike-scan
- sudo git clone https://github.com/stasinopoulos/commix.git 
- sudo git clone https://github.com/sqlmapproject/sqlmap.git 
- sudo git clone https://github.com/CoreSecurity/impacket.git
- sudo git clone https://github.com/samratashok/nishang.git
- sudo git clone https://github.com/SpiderLabs/Responder.git
- sudo git clone https://github.com/sophron/wifiphisher.git
- sudo git clone https://github.com/Dionach/CMSmap.git
- sudo git clone https://github.com/PowerShellMafia/PowerSploit.git
- sudo git clone https://github.com/offensive-security/exploit-database.git
- sudo wget https://download.sysinternals.com/files/SysinternalsSuite.zip


 
