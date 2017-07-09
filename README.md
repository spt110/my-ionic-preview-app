This is a starter template for [Ionic3](http://ionicframework.com/docs/) projects.

```bash
$ sudo npm install -g ionic cordova

$ sudo ionic cordova  platform add android 

$ sudo ionic cordova  platform add iOS 

$ sudo ionic cordova  resources --icon
  
$ sudo npm install -g ios-deploy --unsafe-perm=true


web调试
$ ionic serve



 官方发布教程
 http://ionicframework.com/docs/intro/deploying/

android
1.生成签名文件
keytool -genkey -v -keystore my-release-key.jks -keyalg RSA -keysize 2048 -validity 10000 -alias my-alias
2.发布
ionic cordova  build  android --prod --release
3.签名
jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore my-release-key.jks ./platforms/android/build/outputs/apk/android-release-unsigned.apk my-alias

//ios
1.sudo ionic cordova  platform build iOS --prod --release
2.xcode 免证书真机调试
http://www.jianshu.com/p/5c1fb2cb293c
http://ionicframework.com/docs/intro/deploying/
