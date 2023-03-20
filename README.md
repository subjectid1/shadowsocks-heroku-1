# Personal ShadowSocks proxy server

## Shadowsocks+V2Ray-plugin

Click the button below to deploy to Heroku

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://dashboard.heroku.com/new?button-url=https%3A%2F%2Fgithub.com%2FBurnedScarecrow%2Fshadowsocks-heroku&template=https%3A%2F%2Fgithub.com%2FBurnedScarecrow%2Fshadowsocks-heroku)

## 0. Attention

Deployment requires registration of a heroku account, a email is required when registering a heroku account (otherwise the verification code cannot be brushed out).

An email address that can receive verification codes normally (@qq.com, @163.com are not acceptable):

- gmail (Best)
- Outlook <https://login.live.com/> here.

## 1. Verification

After the server is deployed, open app to display the webpage normally. After the address is filled with the path (for example: <https://test.herokuapp.com/static>), the 403 page is displayed, which means the deployment is successful.

## 2. Client Configuration

QR code address: https://test.herokuapp.com/qr/vpn.png

(Change test to your own app name. If you changed the QR_Path (path to qr png, filled during deployment) variable, also change the corresponding qr_img to the modified one)

Use the client (Shadowsocks recommended) to scan the QR code.

**or**

Use Configuration file -> Address: https://test.herokuapp.com/qr/

(Change test to your own app name)

Copy the details after opening and import it to the client.

**or**

Manual configuration:

```sh
Server: test.herokuapp.com (change test to your app name)
Port: 443
Password: The password filled in during deployment
Encry Method: chacha20-ietf-poly1305 (or other methods you fill in)
Plugin: v2ray
Plugin Transport mode: websocket-tls
Hostname: Same as Server
Path: "/" + value of V2_Path in app Config Vars
```

Those without a client can also download from here (Android):

[shadowsocks](https://github.com/shadowsocks/shadowsocks-android/)

[v2ray-plugin](https://github.com/shadowsocks/v2ray-plugin-android/)

windows:

<https://github.com/shadowsocks/shadowsocks-windows/wiki/Shadowsocks-Windows-%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E>

# Reference

https://github.com/ygcaicn/ss-heroku

https://github.com/xiangrui120/v2ray-heroku-undone

https://hub.docker.com/r/shadowsocks/shadowsocks-libev

https://github.com/shadowsocks/v2ray-plugin
