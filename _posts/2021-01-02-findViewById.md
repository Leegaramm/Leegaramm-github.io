---
layout: post
title: ":tennis: findViewById"
author: "gaaraam"
tags: Android
---

- Empty activity를 생성하면, 그에 맞는 레이아웃(xml) 파일도 생성된다. 그 xml파일은 어디 있느냐??

```kotlin
class Listner : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_listner)
    }
}
```

- 여기서 마지막 부분인 `setContentView(R.layout.activity_listner)` 에서 `activity_listner` 가 새롭게 생성된 레이아웃 파일이다.
- 레이아웃 파일을 만들어보았다.

```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    tools:context=".Listner">

    <TextView
        android:layout_width="100dp"
        android:layout_height="100dp"
        android:text="Hello"
        android:id="@+id/hello"/>

</LinearLayout>
```

- `LinearLayout`으로 구성된, 버튼 하나 가지고 있는 레이아웃이다.
- 이 레이아웃을 activity로 가져가서 동작을 구현시켜야 한다.


```kotlin
import androidx.appcompat.app.AppCompatActivity
import android.widget.TextView
import android.os.Bundle

class Listner : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_listner)
    }

		val textview : TextView = findViewById(R.id.hello) // 이 부분을 추가한다.
}
```
