# Tuya RTC Web Demo

[English](README.md) | [中文版](README_cn.md)
## Overview
The WebRTC SDK helps developers quickly access IPC services.

## Preparation before use
1. Obtain `clientId` and `secret` according to the [Tuya IoT Platform Quick Start](https://developer.tuya.com/en/docs/iot/open-api/quick-start/quick-start1?id=K95ztz9u9t89n).

2. Update `clientId` and `secret` in Demo webrtc.json.

3. Visit the [Tuya open platform authorization page](https://openapi.tuyacn.com/selectAuth?client_id={clientId}&redirect_uri=https://www.example.com/auth&state=1234) and enter the Tuya account Password, agree to authorization, intercept the authorization code `code` in the browser callback URL, where `{clientId}` is the clientId obtained in step 2.

4. Update the `code` in Demo webrtc.json.

5. Select an IPC in the Tuya Smart APP, query the device ID, and update it to the `deviceId` of Demo webrtc.json.

## Example

1. In the Demo source code path, execute `go get` and then execute `go build`.

2. Run `./webrtc-web-sample`.

3. Open `http://localhost:3333` in Chrome, click `Call` to start a WebRTC session.


## Precautions
1. After obtaining the open platform configs, you need to use the string after `/av/u/` in the `result.source_topic.ipc` JSON field as the `from` field in the MQTT Header, so that you can correctly receive the message from the Tuya MQTT service.


## Technical Support

You can get Tuya developer technical support in the following ways:

- Tuya Help Center: [https://support.tuya.com/zh/help](https://support.tuya.com/zh/help)
- Tuya technical ticket platform: [https://iot.tuya.com/council](https://iot.tuya.com/council)
