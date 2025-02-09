# node-red-pushsafer

A [Pushsafer](https://www.pushsafer.com/) API wrapper for Node-RED.

Supports rich notifications and notification templates.

![Pushsafer logo](pushsafer_logo.png)

## Install

Run the following command in your Node-RED user directory - typically `~/.node-red`

    npm install node-red-pushsafer

Or use the palette manager inside of Node-RED

[![npm](https://img.shields.io/npm/v/node-red-pushsafer.svg)](https://www.npmjs.com/package/node-red-pushsafer)

## Required inputs

- `msg.payload` (any): The message of the notification, [see description](https://www.pushsafer.com/pushapi_ext#API-M), [HTML format](https://www.pushsafer.com/pushapi_ext#API-HTML) can be used

## Optional inputs, if provided they will override the template values

- `msg.title` (string): Subject / title of a push-notification, max. 255 characters, [see description](https://www.pushsafer.com/pushapi_ext#API-T)
- `msg.icon` (number): Instead of the default Pushsafer icon, which is displayed with the push notification, you can choose between 177 other icons, [see description](https://www.pushsafer.com/pushapi_ext#API-I)
- `msg.iconcolor` (color): Color of the background of the icon, [see description](https://www.pushsafer.com/pushapi_ext#API-C)
- `msg.sound` (number): Ringtone / Sound which should be played when receiving the push notification, [see description](https://www.pushsafer.com/pushapi_ext#API-S)
- `msg.vibration` (number): How often the device should vibrate when receiving a push-notification, [see description](https://www.pushsafer.com/pushapi_ext#API-V)
- `msg.priority` (number): This priority value determines where the push notification will be put in the notification shade (this sorting affects Android devices only), [see description](https://www.pushsafer.com/pushapi_ext#API-PR)
- `msg.devices` (string): This parameter controls to which devices or device groups the message is sent to, [see description](https://www.pushsafer.com/pushapi_ext#API-D)
- `msg.timetolive` (number): Specifies how long a message should be kept in the client APP until it is automatically deleted, [see description](https://www.pushsafer.com/pushapi_ext#API-L)
- `msg.retry` (number): With the retry / resend parameter, a message will be resent after a certain time, [see description](https://www.pushsafer.com/pushapi_ext#API-RE)
- `msg.expire` (number): With the retry / resend Parameter re, a message will be resent after a certain time, [see description](https://www.pushsafer.com/pushapi_ext#API-EX)
- `msg.confirm` (number): With the confirm Parameter cr, a message will be resent until it is confirmed, [see description](https://www.pushsafer.com/pushapi_ext#API-CR)
- `msg.answer` (number): To respond to push notifications, pass the parameter with the value 1, [see description](https://www.pushsafer.com/pushapi_ext#API-A)
- `msg.answeroptions` (string): predefined answer options divided by a pipe character e.g. Yes|No|Maybe, [see description](https://www.pushsafer.com/pushapi_ext#API-AO)
- `msg.answerforce` (number): to force an answer, pass the parameter with the value 1, [see description](https://www.pushsafer.com/pushapi_ext#API-AF)
- `msg.url` (string): This URL can be opened directly from the push notification or from the client-app, [see description](https://www.pushsafer.com/pushapi_ext#API-U)
- `msg.urltitle` (string): Can set the title of the url, [see description](https://www.pushsafer.com/pushapi_ext#API-UT)
- `msg.image` (string): The path of an image, which will be shown directly in the notification. Local file path or http(s) url, [see description](https://www.pushsafer.com/pushapi_ext#API-P)
- `msg.image2` (string): The path of a second image, which will be shown in the Pushsafer app. Local file path or http(s) url, [see description](https://www.pushsafer.com/pushapi_ext#API-P)
- `msg.image3` (string): The path of a third image, which will be shown in the Pushsafer app. Local file path or http(s) url, [see description](https://www.pushsafer.com/pushapi_ext#API-P)
