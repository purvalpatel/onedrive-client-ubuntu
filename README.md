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
If git clone not working then use below steps:
```bash
[download source](https://raw.githubusercontent.com/purvalpatel/onedrive-client-ubuntu/9dce8b7d3a5e7425f2b86dbded9cfa9e3be97e3c/onedrive.tar.gz)
tar -xvzf onedrive.tar.gz
cd onedrive
./configure
make
sudo make install
```
Here, Your installation is completed.

##### Follow below steps to configure your onedrive account:

Run below command:
```
onedrive
```
It will ask to open link in browser and login with one drive credentials. 

once it is logged in it will ask to copy link of browser then paste on terminal.

<img width="1915" height="658" alt="image" src="https://github.com/user-attachments/assets/974810cb-08bb-4661-80aa-2fe255bf8cf9" />

<img width="1872" height="490" alt="image" src="https://github.com/user-attachments/assets/503ce3cc-1652-47c3-82d4-0ad6b6d09f1e" />

#### verify the configuration with:
```
onedrive --display-config
```

#### Sync file from local to onedrive:

One folder is created in home directory named, OneDrive.
Files which are available in this folder will be synced on OneDrive Storage.

```
onedrive --upload-only --sync
```
