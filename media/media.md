## 各流媒体协议优缺点
### http
* 一般点播用http就可以满足，hls、http-flv
* CDN支持好，适用于大规模直播，rtmp也有CDN支持，但肯定贵（这一点只是参考）


* 直播主要问题是延迟大，无论怎么切片，延迟一般都会在2s以上

### rtmp
* 一般用于直播，延迟能够做到1s以内，但弱网环境下不行
* 直播推流一般用RTMP

* 基于tcp，弱网环境下丢包严重
* adobe私有协议，更新不足，浏览器上需要用flash插件，肯能被H5替代

RTMP是基于FLV来开发的，但是现在FLV在浏览器上各种不兼容，得借助于flash。但是MSE (Media Source Extensions)通过对HTML5中的HTMLMediaElement扩展，使得前端可以对媒体流进行操作，从而支持播放一些流媒体本不支持的格式。例如：https://github.com/Bilibili/flv.js

### webrtc
* W3C标准，主流浏览器和H5支持，相当于各平台都支持（包括不同操作系统和pc/移动端）
* 基于SRTP 和 UDP，弱网情况优化空间大
* 本质上是P2P，通信双方延迟低，是实现“连麦”功能比较好的选择
* 类似于sip适合做视频会议

* ICE、STUN、TURN等传统CDN没有类似服务出现

### rtsp
传统的直播协议，支持udp和tcp，但是
* 浏览器不支持rtsp插件了，flash也不支持rtsp，商业应用受很大限制
* 国内的CDN对RTMP做过优化，而RTSP没有
* 网络中的路由器或防火墙可能对RTSP端口不开放