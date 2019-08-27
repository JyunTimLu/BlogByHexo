---
title: Android ACRA-自動發送CrashReport
date: 2016-06-02 16:11:52
tags: [Android,ACRA]
---
Automated Android Crash Reports with ACRA and Cloudant

<!-- more -->

[參考](http://www.toptal.com/android/automated-android-crash-reports-with-acra-and-cloudant)
Android APP Crash 自動傳錯誤訊息上Cloudant

1.     在Cloudant建立APP錯誤訊息Storage資料庫 
![](/images/android-acra/Image1.png)
2.     在Cloudant建立APP錯誤訊息acralyzer資料庫 
![](/images/android-acra/Image2.png)
3.     取得Ganeral API Keys 將Write權限開啟 紀錄下key與password 
![](/images/android-acra/Image3.png)	
		輸入該網址可以觀看Database Dashboard
		https://{username}.cloudant.com/{acralyzerdatabase}/_design/acralyzer/index.html#/dashboard 
![](/images/android-acra/Image4.png)
4.     Implementing ACRA in your Android project
		將acra-4.5.0.jar 匯入libs
		在AndroidManifest.xml 加入
		![](/images/android-acra/Image5.png)
5.     ACRA class setup
username 處輸入cloudant 帳號,app storage database name 輸入第一步建立的Storage資料庫,key&password輸入第三步取得的key,password
![](/images/android-acra/Image6.png)
6.     DONE~

7.     2017.3.10 呃...更新一下XD 在用過Fabric的Crashlytics後覺得Fabric的功能比ACRA強大太多啦~有AndroidStudio的Plugin, 也不用在Cloudant額外建一個DataBase