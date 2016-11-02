# WebRTC 在Mac OS X 编译

>*目的*
主要是mac平台能够更好地调试WebRTC的源码

## Webrtc的开发
- - -
WebRTC目前支持的平台是Windows，Mac OS X，Linux，Android和iOS平台。

## 开始之前的准备
- - -

Google的chromium项目是用gclient来管理源码的checkout, update等。 gclient是google专门为这种多源项目编写的脚本，它可以将多个源码管理系统中的代码放在一起管理。甚至包括将Git和svn代码放在一起。

[Google工具安装](https://webrtc.org/native-code/development/prerequisite-sw/)

## 获取代码
- - -
*注意：请严格遵守以下步骤,这样可以获取到与系统相关的WebRTC源码*

##### 1.建立WebRTC目录，进入webrtc-checkout,并执行`fetch webrtc`:
```
	mkdir webrtc-checkout
	cd webrtc-checkout
	fetch --nohooks webrtc
	gclient sync
```
##### 2.如何跟踪新的分支(可选)
```
	git config branch.autosetupmerge always
	git config branch.autosetuprebase always
```
##### 3.可以创建新的本地分支(推荐)
```
cd src
git checkout master
git new-branch your-branch-name
```

##### Mac编译
```
gn gen out/Debug-mac
```


