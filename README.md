# AGHCopernicusNode-RED
Node-RED implementation based on subflows for AGH Copernicus

## Installation
### Check if you have Nodejs and NPM installed on your device:
```bash
    node -v
```
```bash
    npm -v
```

##### In case any of them is missing you need to install them:
- Firstly, update list of available packages using:
```bash
    opkg update
```
- To install nodejs:
```bash
    opkg install nodejs
```
- To install npm:
```bash
    opkg install nodejs-npm
```

### Install Node-RED
To install node-RED you need to execute:
```bash
    npm install -g --unsafe-perm node-red
```
It can take some time

### Install Node-RED nodes to talk to serial ports
In order to install this nodes you need to change your current directory to `~/.node-red`. To do that:
```bash
    cd ~/.node-red
```
Then:
```bash
    npm i node-red-node-serialport
```

##### Troubleshooting
There might be some problems with linking after installing nodes for serial port. 
In that case you need to install node-gyp globally:
```bash
    npm install -g node-gyp
```
And then execute following commands:
```bash
    cd ~/.node-red/node_modules/node-red-node-serialport/node_modules/serialport
    node-gyp configure build
```