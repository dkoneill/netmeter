# netmeter

Netmeter is a python application that uses mulay (a bus relay / sender) to transmit various network metrics, such as fping and speedtest.net results.

## Build netmeter
1. Clone this git repository
2. ```cd netmeter```
3. ```python3 setup.py install --user```

## Service installation (systemd)
1. Edit nm-fping.config and adjust
   - send method
   - prefix
   - delay
   - fping targets
   - reporting destination config
2. Edit nm-fping.service and adjust location of configuration file
3. ```sudo cp nm-fping.service /lib/systemd/system/```
4. ```sudo systemctl daemon-reload```
5. ```sudo systemctl enable nm-fping.service```
6. ```sudo service nm-fping start```
