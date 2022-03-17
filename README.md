# Super_live_commerc_server
Welcome to Super Live Commerce! 

## 소개
![ezgif-5-9b897b13cd](https://user-images.githubusercontent.com/49712957/158364719-392452d9-88cb-4af2-9408-caf9b30dc89d.gif)

제작 기간: 2022.02.03 ~ 2022. 3.11
## 주요 기능
- ✅  진행중인 모든 라이브 방송 프리뷰 제공
- ✅  시청자와 스트리머 간 채팅, 하트 보내기
- ✅  시청자 수와 입장시 알림 기능
- ✅  Drag and Drop을 이용한 2채널 동시 시청
- ✅  앱 내 pip 기능
- ✅  스트리머에게 url을 받아 상품페이지로 이동 가능한 배너 생성 (시청 페이지 only)
- ✅  지나간 방송 다시보기

**이후 구현 예정 기능**
- 🟩  다시보기시 채팅, 하트 등 방송 이벤트 보기
- 🟩  홈화면과 동시시청 페이지에서 상품 배너 띄우기

You can see our presentation in 
https://docs.google.com/presentation/d/110ow7Zs_uaOli02OA1jQhR6tVWku5T0aa1aZ9W2iSII/edit?usp=sharing

## 소개
![OnAirSuperLive 포스터](https://user-images.githubusercontent.com/49712957/158327013-9d44cc0b-5fa8-42e7-a53a-1b6b9c7047b2.jpg)
### Server Structure


<img width="924" alt="structure" src="https://user-images.githubusercontent.com/52844717/158049078-3754f482-ad6e-49e9-8ed3-96be9ee6cee2.png">

>Setting

node js version : 14.15.0


java version : 15.0.1


javac version : 15.0.1


nginx version 1.14.0

```bash
node -v
java --version
javac --version
nginx -v

## Prerequisite

- Install NodeJS (https://nodejs.org)
- Install ffmpeg (https://www.ffmpeg.org/download.html). If you are using MacOS just type _brew install ffmpeg_
- MongoDB (https://www.mongodb.com/)
- Nginx-RTMP Server (https://github.com/arut/nginx-rtmp-module). Setting nginx.conf in your '/etc/nginx' directory

Then start MongoDB. Then type the following to terminal

```
# mongo


Then switch to admin database

```
use admin
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
