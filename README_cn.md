# Tuya RTC Web Demo

[English](README.md) | [中文版](README_cn.md)
## 概述
webrtc sdk，方便开发者快速接入ipc业务

## 使用前准备
1. 根据[Tuya开放平台快速入门](https://docs.tuya.com/zh/iot/open-api/quick-start/quick-start1) ，获取`clientId`和`secret`

2. 更新Demo webrtc.json中的`clientId`和`secret`

3. 访问**Tuya开放平台授权页面**  `https://openapi.tuyacn.com/selectAuth?client_id={clientId}&redirect_uri=https://www.example.com/auth&state=1234` ，输入Tuya账号密码，同意授权，截取浏览器回调URL中的授权码`code`，此处`{clientId}`为步骤2中获取的clientId

4. 更新Demo webrtc.json中的`code`

5. 涂鸦智能APP中选中一台IPC，查询设备ID，更新到Demo webrtc.json的`deviceId`

## Example


1. 在Demo源码路径，执行`go get`后执行`go build`

2. 运行`./webrtc-web-sample`

3. Chrome打开`http://localhost:3333`，点击`Call`按钮，即可开始WebRTC会话


## 注意事项
1. 获取开放平台configs后，需要将`result.source_topic.ipc`JSON字段中`/av/u/`后的字符串作为MQTT Header中的from，这样才能正确接受涂鸦MQTT服务的消息


## 技术支持

你可以通过以下方式获得Tuya开发者技术支持：

- 涂鸦帮助中心: [https://support.tuya.com/zh/help](https://support.tuya.com/zh/help)
- 涂鸦技术工单平台: [https://iot.tuya.com/council](https://iot.tuya.com/council)
