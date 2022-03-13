# Super_live_commerc_server
Welcome to Super Live Commerce! 
![logo](https://user-images.githubusercontent.com/52844717/158049041-2bf0a3f0-e662-4b48-80e2-2189529ac1a1.png)

Our Server Structure
<img width="924" alt="structure" src="https://user-images.githubusercontent.com/52844717/158049078-3754f482-ad6e-49e9-8ed3-96be9ee6cee2.png">

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

Client : https://github.com/TeamGreyOrg/super_live_client.git

## Config

Then we check the _src/config.js_ to edit the server information. Fill in your localhost server information (Ip address, Port)

```js
export const SOCKET_IO_SERVER = 'http://192.168.0.14:3333'; // Edit this
export const RTMP_SERVER = 'rtmp://192.168.0.14'; // Edit this
export const HTTP = 'rtmp://192.168.0.14:8000'; // Edit this
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


