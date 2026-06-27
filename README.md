The AntScope2 software is designed to support various models of RigExpert analyzers under various operating systems.

Windows: QT5, QT Creator 2 and higher

Linux: Qt 6 and qmake

Ubuntu 24.04 build dependencies:

```sh
sudo apt-get install qmake6 qt6-base-dev qt6-base-dev-tools qt6-connectivity-dev qt6-serialport-dev qt6-tools-dev-tools libusb-1.0-0-dev build-essential
```

Build:

```sh
qmake6 AntScope.pro CONFIG+=release
make -j$(nproc)
```

The Linux binary is created at `build/release/AntScope2`. The qmake post-link step copies the required runtime data files to `build/`, where the application expects them for local builds.

Mac OS: to do
