# Super_live_commerc_client

node js version : 14.15.0
java version : 15.0.1
javac version : 15.0.1
react native version 6.4.0

```bash
node -v
java --version
javac --version
react-native --version
```


## Getting Started

We need the RTMP server first. Download the repository below and follow the README information.

Server : https://github.com/TeamGreyOrg/super_live_server.git

## Config

Then we check the _src/config.js_ to edit the server information. Fill in your localhost server information (Ip address, Port)

```js
export const SOCKET_IO_SERVER = 'http://192.168.0.14:3333'; // Edit this
export const RTMP_SERVER = 'rtmp://192.168.0.14'; // Edit this
```

## Install package

```bash
npm install 

or 

yarn install
```

### Android

```bash
npm run android 

or

yarn run run-android
```


