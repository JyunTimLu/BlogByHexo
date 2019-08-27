---
title: Android 依賴Github Project
date: 2016-09-26 09:21:52
tags: [Android,Github]
---
Dependencies Project From Github

<!-- more -->
在Project的build.gradle下加入
``` bash
allprojects {
    repositories { 
        jcenter()
        maven { url "https://jitpack.io" }
    }
}
```

在Application build.gradle 加入需要引入的Github Project
``` java
dependencies {
    compile 'com.github.User:Repo:Tag'
}
```

開發過程中還沒有Release Tag 可以用commit sha 替代
