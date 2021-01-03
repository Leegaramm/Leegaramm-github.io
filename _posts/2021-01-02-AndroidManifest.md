---
layout: post
title: "AndroidManifest.xml을 읽어보자."
author: "gaaraam"
tags: Android
---
* 모든 앱 프로젝트에는 `Android Manifest.xml`파일이 있어야 한다.
* 매니페스트 파일은 Android 빌드 도구, Android 운영체제 및 Google Play에 앱에 관한 필수 정보를 설명한다.
* 매니페스트 파일은 다른 여러 가지도 설명하지만 특히 다음과 같은 내용을 선언해야 합니다.
* 참고 : https://developer.android.com/guide/topics/manifest/manifest-intro
<br>

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
