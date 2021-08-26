# ccminer for ARM (RK3328)

Based on https://github.com/monkins1010/ccminer/tree/ARM

Git and Build Process:
```
sudo apt-get update
sudo apt-get install libcurl4-openssl-dev libssl-dev libjansson-dev automake autotools-dev build-essential -y
sudo apt-get install clang-12 lld-12 -y
git clone https://github.com/mwash-1/ccminer-rk3328.git
cd ccminer-rk3328
chmod +x build.sh configure.sh autogen.sh
./build.sh

sudo vi /etc/systemd/system/verus.service
<contents>
systemctl daemon-reload
systemctl enable verus
systemctl start verus
journalctl -f -u verus
```

Compile on Linux
----------------

Please see [INSTALL](https://github.com/tpruvot/ccminer/blob/linux/INSTALL) file or [project Wiki](https://github.com/tpruvot/ccminer/wiki/Compatibility)
