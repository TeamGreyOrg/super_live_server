# Super_live_commerc_server
Welcome to Super Live Commerce! 

Our Server Structure

<img width="924" alt="structure" src="https://user-images.githubusercontent.com/52844717/158049078-3754f482-ad6e-49e9-8ed3-96be9ee6cee2.png">

node js version : 14.15.0


java version : 15.0.1


javac version : 15.0.1


react native version 6.4.0


nginx version 1.14.0

```bash
node -v
java --version
javac --version
react-native --version
nginx -v

## Prerequisite

- Install NodeJS (https://nodejs.org)
- Install ffmpeg (https://www.ffmpeg.org/download.html). If you are using MacOS just type _brew install ffmpeg_
- MongoDB (https://www.mongodb.com/)
- Nginx-RTMP Server (https://github.com/arut/nginx-rtmp-module). Setting nginx.conf in your '/etc/nginx' directory

Then start MongoDB. Then type the following to terminal

```
# mongo
```

Then switch to admin database

```
> use admin
```

Then create user admin

```
db.createUser({
  user: 'admin',
  pwd: '123456',
  roles: [
    { role: 'userAdminAnyDatabase', db: 'admin' },
    { role: 'dbAdminAnyDatabase', db: 'admin' },
    { role: 'readWriteAnyDatabase', db: 'admin' }
  ]
})
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

### Streaming Format provided 
mp4/hls/dash

> Adaptive Bitrate Streaming Feature

![Adaptive Bitrate Streaming](https://user-images.githubusercontent.com/52844717/158050150-abb4a790-f329-4d94-857e-5a61f799090d.png)
