---
layout: post
title: "AndroidManifest.xml을 읽어보자."
author: "gaaraam"
tags: Android
---

```xml
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.example.androidstudy">

    <application
        android:allowBackup="true"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="true"
        android:theme="@style/Theme.AndroidStudy">
        <activity android:name=".MainActivity">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>

</manifest>
```

```xml
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.example.androidstudy">
```

- `package` 는 패키지명, 내 앱의 이름
- `android:allowBackup="true"` 는 내가 앱을 지우고 다시 깔았을 때, 전에 로그인했던 정보나 데이터가 기억되어 있는지, 백업되어 있는지 옵션
- `android:icon="@mipmap/ic_launcher"` 아이콘 이미지
- `android:supportsRtl="true"` 중동권에서 오른쪽에서 왼쪽으로 읽는 방식도 지원
- `<category android:name="android.intent.category.LAUNCHER" />` 앱을 키자마자 나오는 화면, 런처화면, 런처 액티비티