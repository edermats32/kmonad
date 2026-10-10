# kmonad
Kmonad config

# Setup on Debian
```sh
sudo groupadd -f uinput
```
```sh
sudo usermod -aG input,uinput $USER
```
`/etc/udev/rules.d/90-kmonad.rules`
```
KERNEL=="uinput", MODE="0660", GROUP="uinput", OPTIONS+="static_node=uinput"
```
```sh
sudo modprobe uinput
```
```sh
sudo udevadm control --reload && sudo udevadm trigger
```
```sh
reboot
```
**Download this repo**
```sh
mkdir -p mkdir ~/.config/systemd/user/
```
```sh
mkdir 
```
```sh
cp kmonad@.service ~/.config/systemd/user/
```
```sh
mkdir ~/config/kmonad
```
```sh
mv main.kbd ~/config/kmonad/
```
```sh
mkdir ~/.local/bin
```
```sh
mv kmonad ~/.local/bin/
```
```sh
chmod +x ~/.local/bin/kmonad
```
```sh
systemctl --user enable --now kmonad@main
```
