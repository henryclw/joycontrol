```bash
apt install python3-dbus python3-pip libhidapi-hidraw0 libbluetooth-dev bluez
pip3 install aioconsole hid==1.0.4 crc8 --break-system-packages
nano /lib/systemd/system/bluetooth.service
systemctl daemon-reload
systemctl restart bluetooth.service

python3 run_controller_cli.py PRO_CONTROLLER
python3 run_controller_cli.py -r auto PRO_CONTROLLER
```


```bash
hcitool cmd 0x3f 0x0031 0x66 0x55 0x44 0xCB 0x58 0x94
nano /etc/bluetooth/main.conf
```