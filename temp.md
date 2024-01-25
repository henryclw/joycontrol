```bash
apt install python3-dbus libhidapi-hidraw0 libbluetooth-dev bluez
pip3 install aioconsole hid==1.0.4 crc8 --break-system-packages
systemctl daemon-reload
systemctl restart bluetooth.service

python3 run_controller_cli.py PRO_CONTROLLER
python3 run_controller_cli.py -r auto PRO_CONTROLLER
```