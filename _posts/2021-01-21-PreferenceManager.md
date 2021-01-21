---
layout: post
title: ":tennis: 사용되지 않는 PreferenceManager와 kotlin android extensions"
author: "gaaraam"
tags: Android
---

구글 안드로이드 문서에서 [PreferenceManager](https://developer.android.com/reference/android/preference/PreferenceManager) 항목을 보면,

> This class was deprecated in API level 29.
Use the AndroidX Preference Library for consistent behavior across all devices. For more information on using the AndroidX Preference Library see Settings.

빨간 글씨로 무시무시한 경고문을 띄운다. 실제 안드로이드 스튜디오에서도 마찬가지로, 자동완성에서 가운데 줄이 그어져 있는 것을 확인할 수가 있다. deprecated 되어 있으니, AndroidX 환경 설정 라이브러리를 사용하라는 이야기인데, 이를 사용하는 방법은 매우 간단하다.

build.gradle(Module)의 dependencies를 찾은 뒤에,
```
    implementation 'androidx.preference:preference:1.1.1'
```
이 한 줄을 입력해서 추가해주면 된다. 그리고 `sync now`를 클릭해주면, 이 라이브러리를 사용할 수 있다.

`Kotlin Android Extensions` 역시 최근에 deprecated된 대표적인 라이브러리인데, 이는 여러가지 취약한 부분이 존재하기 때문에, 공식적으로 `ViewBinding`의 방법으로 대체되었다. 그래도 굳이 쓰고싶다면, 

build.gradle(Module)의 plugin에
```
    id 'kotlin-android-extensions'
```
를 입력해주면 사용할 수 있다. 사용하는 것은 본인 자유지만, 아니 자유가 아니다. 그냥 이런게 있었다고만 여기고, **사용하지 말자.**

`kotlin-android-extensions`를 사용한 후 빌드하면 빌드창에

> The 'kotlin-android-extensions' Gradle plugin is deprecated. Please use this migration guide (https://goo.gle/kotlin-android-extensions-deprecation) to start working with View Binding (https://developer.android.com/topic/libraries/view-binding) and the 'kotlin-parcelize' plugin.

이런 메시지가 뜨는데, 사용하지 말 것을 구글이 공식적이고도 아주 강력하게 요청하고 있는 것을 다시 한 번 확인할 수 있다.


