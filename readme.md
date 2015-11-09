创建一个 Ionic 工程模板


## 配置

先配置好 nodejs 环境

```
npm install -g cordova
npm install -g ionic
```


## 创建一个新项目

```
ionic start myapp

```

添加 android 支持

```
cd myapp
ionic platform add android
```

构建

```
ionic build android
```

ionic 框架对 cordova 项目工程命令进行了包装，可以直接使用 crodova 命令

cordova 工程创建

```
cordova create myapp
cd myapp
cordova platform add android
cordova build android
```

> 注意: ionic 不支持中文路径，不然构建不成功

cordova 插件添加

```
cordova plugin add org.apache.cordova.geolocation
cordova plugin add org.apache.cordova.file
cordova plugin add org.apache.cordova.dialogs
cordova plugin add org.apache.cordova.device
cordova plugin add org.apache.cordova.console
cordova plugin add org.apache.cordova.camera
```

插件删除

```
cordova plugin remove (输入插件地址)  移除插件
```


phoneGap 云端构建

```
phonegap remote build ios
phonegap remote build android
```


## 构建，测试，部署


通过 USB 直接安装到真机

```
cordova run android
```


在本机调试 SPA

```
cd myapp
ionic serve
```

## Ionic 项目目录

```
myapp/
   | /.bowerrc
   | /.editorconfig
   | /.gitignore
   | /bower.json
   | /config.xml
   | /gulpfile.js
   | /index.md
   | /ionic.project
   | /package.json
   |-- hooks/
   |        /README.md
   |   |-- after_prepare/
   |   |                /010_add_platform_class.js
   |-- plugins/
   |          /fetch.json
   |   |-- cordova-plugin-console/
   |   |                         /CONTRIBUTING.md
   |   |                         /LICENSE
   |   |                         /NOTICE
   |   |                         /package.json
   |   |                         /plugin.xml
   |   |                         /README.md
   |   |                         /RELEASENOTES.md
   |   |   |-- doc/
   |   |   |   |-- de/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- es/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- fr/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- it/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- ja/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- ko/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- pl/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- ru/
   |   |   |   |     /index.md
   |   |   |   |-- zh/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |-- src/
   |   |   |   |-- ios/
   |   |   |   |      /CDVLogger.h
   |   |   |   |      /CDVLogger.m
   |   |   |   |-- ubuntu/
   |   |   |   |         /console.cpp
   |   |   |   |         /console.h
   |   |   |   |-- wp/
   |   |   |   |     /DebugConsole.cs
   |   |   |-- tests/
   |   |   |        /plugin.xml
   |   |   |        /tests.js
   |   |   |-- www/
   |   |   |      /console-via-logger.js
   |   |   |      /logger.js
   |   |-- cordova-plugin-device/
   |   |                        /CONTRIBUTING.md
   |   |                        /LICENSE
   |   |                        /NOTICE
   |   |                        /package.json
   |   |                        /plugin.xml
   |   |                        /README.md
   |   |                        /RELEASENOTES.md
   |   |   |-- doc/
   |   |   |   |-- de/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- es/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- fr/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- it/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- ja/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- ko/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- pl/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- ru/
   |   |   |   |     /index.md
   |   |   |   |-- zh/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |-- src/
   |   |   |   |-- android/
   |   |   |   |          /Device.java
   |   |   |   |-- blackberry10/
   |   |   |   |               /index.js
   |   |   |   |-- browser/
   |   |   |   |          /DeviceProxy.js
   |   |   |   |-- firefoxos/
   |   |   |   |            /DeviceProxy.js
   |   |   |   |-- ios/
   |   |   |   |      /CDVDevice.h
   |   |   |   |      /CDVDevice.m
   |   |   |   |-- tizen/
   |   |   |   |        /DeviceProxy.js
   |   |   |   |-- ubuntu/
   |   |   |   |         /device.cpp
   |   |   |   |         /device.h
   |   |   |   |         /device.js
   |   |   |   |-- windows/
   |   |   |   |          /DeviceProxy.js
   |   |   |   |-- wp/
   |   |   |   |     /Device.cs
   |   |   |-- tests/
   |   |   |        /plugin.xml
   |   |   |        /tests.js
   |   |   |-- www/
   |   |   |      /device.js
   |   |-- cordova-plugin-splashscreen/
   |   |                              /CONTRIBUTING.md
   |   |                              /LICENSE
   |   |                              /NOTICE
   |   |                              /package.json
   |   |                              /plugin.xml
   |   |                              /README.md
   |   |                              /RELEASENOTES.md
   |   |   |-- doc/
   |   |   |   |-- de/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- es/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- fr/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- it/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- ja/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- ko/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- pl/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- ru/
   |   |   |   |     /index.md
   |   |   |   |-- zh/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |-- src/
   |   |   |   |-- android/
   |   |   |   |          /SplashScreen.java
   |   |   |   |-- blackberry10/
   |   |   |   |               /index.js
   |   |   |   |-- browser/
   |   |   |   |          /SplashScreenProxy.js
   |   |   |   |-- ios/
   |   |   |   |      /CDVSplashScreen.h
   |   |   |   |      /CDVSplashScreen.m
   |   |   |   |      /CDVViewController+SplashScreen.h
   |   |   |   |      /CDVViewController+SplashScreen.m
   |   |   |   |-- tizen/
   |   |   |   |        /SplashScreenProxy.js
   |   |   |   |-- ubuntu/
   |   |   |   |         /splashscreen.cpp
   |   |   |   |         /splashscreen.h
   |   |   |   |-- wp/
   |   |   |   |     /ResolutionHelper.cs
   |   |   |   |     /SplashScreen.cs
   |   |   |-- tests/
   |   |   |        /plugin.xml
   |   |   |        /tests.js
   |   |   |   |-- ios/
   |   |   |   |      /package.json
   |   |   |   |      /README.md
   |   |   |       |-- CDVSplashScreenTest/
   |   |   |       |                      /.npmignore
   |   |   |       |   |-- CDVSplashScreenLibTests/
   |   |   |       |   |                          /ImageNameTest.m
   |   |   |       |   |                          /ImageNameTestDelegates.h
   |   |   |       |   |                          /ImageNameTestDelegates.m
   |   |   |       |   |                          /Info.plist
   |   |   |       |   |-- CDVSplashScreenTest.xcodeproj/
   |   |   |       |   |                                /project.pbxproj
   |   |   |       |       |-- project.xcworkspace/
   |   |   |       |       |                      /contents.xcworkspacedata
   |   |   |       |       |   |-- xcshareddata/
   |   |   |       |       |   |               /CDVSplashScreenTest.xccheckout
   |   |   |       |       |-- xcshareddata/
   |   |   |       |           |-- xcschemes/
   |   |   |       |           |            /CDVSplashScreenLib.xcscheme
   |   |   |       |           |            /CDVSplashScreenLibTests.xcscheme
   |   |   |       |-- CDVSplashScreenTest.xcworkspace/
   |   |   |       |                                  /contents.xcworkspacedata
   |   |   |       |   |-- xcshareddata/
   |   |   |       |   |               /CDVSplashScreenTest.xccheckout
   |   |   |       |       |-- xcschemes/
   |   |   |       |       |            /CordovaLib.xcscheme
   |   |   |       |-- doc/
   |   |   |           |-- de/
   |   |   |           |     /README.md
   |   |   |           |-- es/
   |   |   |           |     /README.md
   |   |   |           |-- fr/
   |   |   |           |     /README.md
   |   |   |           |-- it/
   |   |   |           |     /README.md
   |   |   |           |-- ja/
   |   |   |           |     /README.md
   |   |   |           |-- ko/
   |   |   |           |     /README.md
   |   |   |           |-- pl/
   |   |   |           |     /README.md
   |   |   |           |-- zh/
   |   |   |           |     /README.md
   |   |   |-- www/
   |   |   |      /splashscreen.js
   |   |       |-- windows/
   |   |       |          /SplashScreenProxy.js
   |   |-- cordova-plugin-statusbar/
   |   |                           /CONTRIBUTING.md
   |   |                           /LICENSE
   |   |                           /NOTICE
   |   |                           /package.json
   |   |                           /plugin.xml
   |   |                           /README.md
   |   |                           /RELEASENOTES.md
   |   |   |-- doc/
   |   |   |   |-- de/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- es/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- fr/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- it/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- ja/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- ko/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- pl/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |   |-- ru/
   |   |   |   |     /index.md
   |   |   |   |-- zh/
   |   |   |   |     /index.md
   |   |   |   |     /README.md
   |   |   |-- src/
   |   |   |   |-- android/
   |   |   |   |          /StatusBar.java
   |   |   |   |-- ios/
   |   |   |   |      /CDVStatusBar.h
   |   |   |   |      /CDVStatusBar.m
   |   |   |   |-- windows/
   |   |   |   |          /StatusBarProxy.js
   |   |   |   |-- wp/
   |   |   |   |     /StatusBar.cs
   |   |   |-- tests/
   |   |   |        /plugin.xml
   |   |   |        /tests.js
   |   |   |-- www/
   |   |   |      /statusbar.js
   |   |-- cordova-plugin-whitelist/
   |   |                           /CONTRIBUTING.md
   |   |                           /LICENSE
   |   |                           /NOTICE
   |   |                           /package.json
   |   |                           /plugin.xml
   |   |                           /README.md
   |   |                           /RELEASENOTES.md
   |   |                           /whitelist.js
   |   |   |-- src/
   |   |       |-- android/
   |   |       |          /WhitelistPlugin.java
   |   |       |-- ios/
   |   |       |      /CDVNavigationWhitelistPlugin.h
   |   |       |      /CDVNavigationWhitelistPlugin.m
   |   |-- ionic-plugin-keyboard/
   |   |                        /LICENSE
   |   |                        /package.json
   |   |                        /plugin.xml
   |   |                        /README.md
   |       |-- src/
   |       |   |-- android/
   |       |   |          /IonicKeyboard.java
   |       |   |-- blackberry10/
   |       |   |               /index.js
   |       |   |   |-- native/
   |       |   |   |         /.cproject
   |       |   |   |         /.project
   |       |   |       |-- device/
   |       |   |       |         /libKeyboard.so
   |       |   |       |   |-- public/
   |       |   |       |   |         /json_reader.o
   |       |   |       |   |         /json_value.o
   |       |   |       |   |         /json_writer.o
   |       |   |       |   |         /plugin.o
   |       |   |       |   |         /tokenizer.o
   |       |   |       |   |-- src/
   |       |   |       |   |      /CallKeyboard.o
   |       |   |       |   |      /keyboard_js.o
   |       |   |       |   |      /keyboard_ndk.o
   |       |   |       |   |      /Logger.o
   |       |   |       |-- public/
   |       |   |       |         /json_batchallocator.h
   |       |   |       |         /json_internalarray.inl
   |       |   |       |         /json_internalmap.inl
   |       |   |       |         /json_reader.cpp
   |       |   |       |         /json_value.cpp
   |       |   |       |         /json_valueiterator.inl
   |       |   |       |         /json_writer.cpp
   |       |   |       |         /plugin.cpp
   |       |   |       |         /plugin.h
   |       |   |       |         /tokenizer.cpp
   |       |   |       |         /tokenizer.h
   |       |   |       |   |-- json/
   |       |   |       |   |       /autolink.h
   |       |   |       |   |       /config.h
   |       |   |       |   |       /features.h
   |       |   |       |   |       /forwards.h
   |       |   |       |   |       /json.h
   |       |   |       |   |       /reader.h
   |       |   |       |   |       /value.h
   |       |   |       |   |       /writer.h
   |       |   |       |-- simulator/
   |       |   |       |            /libKeyboard.so
   |       |   |       |   |-- public/
   |       |   |       |   |         /json_reader.o
   |       |   |       |   |         /json_value.o
   |       |   |       |   |         /json_writer.o
   |       |   |       |   |         /plugin.o
   |       |   |       |   |         /tokenizer.o
   |       |   |       |   |-- src/
   |       |   |       |   |      /CallKeyboard.o
   |       |   |       |   |      /keyboard_js.o
   |       |   |       |   |      /keyboard_ndk.o
   |       |   |       |   |      /Logger.o
   |       |   |       |-- src/
   |       |   |       |      /keyboard_js.cpp
   |       |   |       |      /keyboard_js.hpp
   |       |   |       |      /keyboard_ndk.cpp
   |       |   |       |      /keyboard_ndk.hpp
   |       |   |       |      /Logger.cpp
   |       |   |       |      /Logger.hpp
   |       |   |-- ios/
   |       |   |      /IonicKeyboard.h
   |       |   |      /IonicKeyboard.m
   |       |   |      /UIWebViewExtension.h
   |       |   |      /UIWebViewExtension.m
   |       |   |-- windows/
   |       |   |          /KeyboardProxy.js
   |       |-- www/
   |           |-- android/
   |           |          /keyboard.js
   |           |-- ios/
   |           |      /keyboard.js
   |-- scss/
   |       /ionic.app.scss
   |-- www/
   |      /index.html
       |-- css/
       |      /style.css
       |-- img/
       |      /adam.jpg
       |      /ben.png
       |      /ionic.png
       |      /max.png
       |      /mike.png
       |      /perry.png
       |-- js/
       |     /app.js
       |     /controllers.js
       |     /services.js
       |-- lib/
       |   |-- ionic/
       |   |        /version.json
       |       |-- css/
       |       |      /ionic.css
       |       |      /ionic.min.css
       |       |-- fonts/
       |       |        /ionicons.eot
       |       |        /ionicons.svg
       |       |        /ionicons.ttf
       |       |        /ionicons.woff
       |       |-- js/
       |       |     /ionic-angular.js
       |       |     /ionic-angular.min.js
       |       |     /ionic.bundle.js
       |       |     /ionic.bundle.min.js
       |       |     /ionic.js
       |       |     /ionic.min.js
       |       |   |-- angular/
       |       |   |          /angular-animate.js
       |       |   |          /angular-animate.min.js
       |       |   |          /angular-resource.js
       |       |   |          /angular-resource.min.js
       |       |   |          /angular-sanitize.js
       |       |   |          /angular-sanitize.min.js
       |       |   |          /angular.js
       |       |   |          /angular.min.js
       |       |   |-- angular-ui/
       |       |   |             /angular-ui-router.js
       |       |   |             /angular-ui-router.min.js
       |       |-- scss/
       |       |       /ionic.scss
       |       |       /_action-sheet.scss
       |       |       /_animations.scss
       |       |       /_backdrop.scss
       |       |       /_badge.scss
       |       |       /_bar.scss
       |       |       /_button-bar.scss
       |       |       /_button.scss
       |       |       /_checkbox.scss
       |       |       /_form.scss
       |       |       /_grid.scss
       |       |       /_items.scss
       |       |       /_list.scss
       |       |       /_loading.scss
       |       |       /_menu.scss
       |       |       /_mixins.scss
       |       |       /_modal.scss
       |       |       /_platform.scss
       |       |       /_popover.scss
       |       |       /_popup.scss
       |       |       /_progress.scss
       |       |       /_radio.scss
       |       |       /_range.scss
       |       |       /_refresher.scss
       |       |       /_reset.scss
       |       |       /_scaffolding.scss
       |       |       /_select.scss
       |       |       /_slide-box.scss
       |       |       /_spinner.scss
       |       |       /_tabs.scss
       |       |       /_toggle.scss
       |       |       /_transitions.scss
       |       |       /_type.scss
       |       |       /_util.scss
       |       |       /_variables.scss
       |           |-- ionicons/
       |           |           /ionicons.scss
       |           |           /_ionicons-font.scss
       |           |           /_ionicons-icons.scss
       |           |           /_ionicons-variables.scss
       |-- templates/
       |            /chat-detail.html
       |            /tab-account.html
       |            /tab-chats.html
       |            /tab-dash.html
       |            /tabs.html

```


## 服务器端

./server

安装相关包

```
cd server
npm install
node server
```

**测试REST 服务**

- http://localhost:5000/sessions (for a list of conference sessions returned as a JSON document)
- http://localhost:5000/sessions/1 (for information about a specific session )



## 开发

新建立的应用程序框架，关注点在以下几点：

1. 路由
2. 视图              试图需要了解 ionic 的组件
3. 控制器            控制器里完成任务后状态的返回
4. service           中间层可以放在 service.js
5. cordova 插件      需要的 cordova 插件添加更新


导航视图 ion-nav-view

```
<ion-nav-view>
<!--模板内容将被插入此处-->
</ion-nav-view>
```

模板视图 ion-view

```
<script id="..." type="text/ng-template">
<ion-view>
<!--模板视图内容-->
</ion-view>
</script>
```

导航栏 ion-nav-bar
```
<ion-nav-bar></ion-nav-bar>
```

回退按钮 ion-nav-back-button

```
<ion-nav-bar>
<ion-nav-back-button></ion-nav-back-button>
</ion-nav-bar>
```

标题栏 ion-header-bar
```
<ion-header-bar>...</ion-header-bar>
```

页脚栏 : ion-footer-bar
```
<ion-footer-bar>...</ion-footer-bar>
```

内容区 ion-content

```
<ion-content>...</ion-content>
```

滚动框 ion-scroll

```
<ion-scroll>
<!--content-->
</ion-scroll>
```

拉动刷新 ion-refresher

```
<ion-refresher></ion-refresher>
```

滚动刷新 ion-infinite-scroll

```
<ion-infinite-scroll on-infinite="">...</ion-infinite-scroll>
```

内联模板 : script
```
<script type="text/ng-template" id="a.html">
　　<p>This is the content of the template.</p>
</script>
```

定制样式

```
<ion-nav-back-button class="button-clear">
<i class="icon ion-ios-arrow-back"></i> 返回
</ion-nav-back-button>
```


## links

- https://github.com/ccoenraets?tab=repositories
- http://www.cnblogs.com/parry/p/issues_about_build_hybrid_app_with_ionic.html
- http://www.cnblogs.com/powertoolsteam/p/4775059.html    项目完整流程
- http://www.cnblogs.com/cube/p/4086645.html          使用内联模板
-