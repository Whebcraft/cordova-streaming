# Cordova Audio Streaming Plugin

   This plugin provides an implementation of an Android service library which uses AAC Player. 
   Ready to use Streaming Player Service. (Background Player Service).

## Notifications
Nice notification to control the service when it's in running in the background


## Supported Platforms

- Android

## Supported Streaming URLs Format

- http://website.com:1232
- http://website.com/file.pls
- http://website.com/file.ram
- http://website.com/file.wax
- http://website.com/file.m4a
- http://website.com/file.mp3

### Installation

This requires phonegap/cordova CLI 3.0+

- Cordova CLI

```sh
cordova plugin add https://github.com/whebcraft/cordova-streaming.git
```


- Phonegap Build

```sh
    <plugin spec="https://github.com/whebcraft/cordova-streaming.git" source="git" />
```


### Quick Example
```js

 document.addEventListener('deviceready', onDeviceReady, false);

function onDeviceReady() {
  Stream.initialize(Successcallback, errorFunction);
}

function Successcallback(status){

}

```

### `status`

String | Description
--------- | ------------
`STOPPED-FROM-NOTIFICATION` | Streaming was stopped from the notification bar.
`STOPPED-FROM-APP` | Streaming was stopped from the app.

```js

var url = 'http://hayatmix.net/;yayin.mp3.m3u';
var title = 'My Stream Title';
var subtitle = 'My Stream Subtitle';

 // Start Streaming...
 Stream.play(successFunction, errorFunction, url, title, subtitle);

 // Stop Streaming...
 Stream.stop(successFunction, errorFunction);
```

License
--------


    Copyright 2016 Whebcraft.

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
