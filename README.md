There’s no official Microsoft OneDrive client for Linux.

This project is regarding installation of onedrive client for ubuntu 24.04. 

Best Option: onedrive by abraunegg
A well-maintained, full-featured command-line OneDrive client for Linux.

Features:
-------------
Full support for OneDrive personal, business, and SharePoint
Sync from OneDrive → local or bi-directional
Automatically sync via systemd service
Supports selective sync via config

Installation:
------------------

#### Dependencies:
```bash
sudo apt install build-essential git curl libcurl4-openssl-dev \
    libsqlite3-dev pkg-config libssl-dev libnotify-dev \
    libxml2-dev libmagic-dev ldc libdbus-1-dev
```
run script with below command or download script from [here](https://raw.githubusercontent.com/purvalpatel/onedrive-client-ubuntu/9dce8b7d3a5e7425f2b86dbded9cfa9e3be97e3c/rustup-init.sh):
```
curl -fsS https://raw.githubusercontent.com/purvalpatel/onedrive-client-ubuntu/9dce8b7d3a5e7425f2b86dbded9cfa9e3be97e3c/rustup-init.sh | sh
```
#### package compilation and installation:
```bash
git clone https://github.com/abraunegg/onedrive.git
cd onedrive
./configure
make
sudo make install
```
If git clone not working then download source code from:

