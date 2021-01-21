---
layout: post
title: "[안드로이드] LinearLayout 입문"
author: "gaaraam"
tags: Android
---

- `Layout`에 해당하는 요소가 부모가 될 수 있다
- 그 외 `viewcomponent`들이 자식요소가 된다
- 자식요소를 나타내는 부분에서는 화면의 배치를 조정할 수 없다. 화면의 배치는 부모요소에서 결정한다.

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical" 
		tools:context=".MainActivity">

    <TextView
        android:text="안녕하세요"
        android:layout_width="wrap_content"
        android:textSize="40dp"
        android:layout_height="wrap_content"/>

    <TextView
        android:text="안녕히계세요"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content">
        </TextView>

</LinearLayout>
```

- 다음 코드에서 `LinearLayout`에 해당하는 부분이 부모요소, 각각의 `textview` 가 자식요소
- `orientation`이라는 속성을 살펴보면, `vertical`은 자식요소를 수직으로 나열하는 것, `horizontal`로 바꾸면 자식요소를 수평으로 나열하게 된다.
- `android:layout_width="match_parent"` → 가로 폭을 모두 사용하겠다
- `LinearLayout`은 자식 요소들을 수직 수평으로 어떻게 배치할지를 알려주는 부모요소. `orientation`은 `LinearLayout`에서만 쓸 수 있다.
- `ScrollView` 에서는 `android:fillViewport="true"`를 무조건 넣어준다. 넣어줘야 에러가 나지 않는다.
- `ScrollView`는 자식뷰를 하나만 가질 수 있다.
