# udev
Udev rules for crazyflie and platformio (for arduino)  

- To be copied in `/etc/udev/rules.d`  

- For crazyflie client, using plugdev user is mandatory so, if group does not exists (fedora):
```sh
groupadd plugdev
```

- And for adding current user in group :
```sh
sudo usermod -a -G plugdev $USER
```
Need to log off and on after adding user in group

- To reload udev rules:
```sh
sudo udevadm control --reload-rules
sudo udevadm trigger
```
