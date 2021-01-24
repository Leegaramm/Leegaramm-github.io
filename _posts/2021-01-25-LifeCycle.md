---
layout: post
title: "[안드로이드] 생명주기"
author: "gaaraam"
tags: Android
---

**Fragment LifeCycle은 Activity LifeCycle과 밀접한 관련이 있다.**

## Activity LifeCycle

`onCreate()` 메서드가 실행되면서 액티비티가 생성된다.

* 액티비티가 초기화되지만 아직 화면에 보이지 않는다.

`onStart()`메서드가 실행되면서 액티비티가 시작된다.

* 액티비티가 보이지만 포커스를 갖지 않는다.

`onResume()` 메서드가 실행되면서 액티비티가 재개된다.

* 액티비티가 보이며 포커스를 가진다.

`onPause()` 메서드가 실행되면서 액티비티가 정지한다.

* 액티비티가 보이지 않는 상태지만 더 이상 포커스를 갖지 않는다.

`onStop()` 메서드가 호출되면서 액티비티가 중지한다.

* 더 이상 보이지 않지만 아직 존재하는 상태이다.

`onDestroy()` 메서드가 실행되면서 액티비티가 종료.

* 액티비티가 더 이상 존재하지 않는다.

## Fragment LifeCycle

> `액티비티 생명주기`
>   * `프래그먼트 생명주기`  
>   * `프래그먼트 생명주기`

`onCreate()`

  * `onAttach(Context)` : 프래그먼트가 컨텍스트에 연결되었을 때 호출된다.
  * `onCreate(Budle)` : 프래그먼트 초기 설정 등의 작업을 하는 곳이다.
  * `onCreateView(LayoutInflator, ViewGroup, Bundle)` : 프래그먼트는 여기서 레이아웃 인플레이터로 자신의 뷰를 만든다.
  * `onActivityCreated(Bundle)` : 액티비티의 `onCreate()` 메서드가 완료되면 호출된다.
  
`onStart()`

  * `onStart()` : 프래그먼트가 보이는 상태가 되기 직전에 호출된다.
  
`onResume()`

  * onResume\(\) : 프래그먼트가 보이는 상태면서 액티비티가 실행중일 때 호출된다.
  
`onPause()`

  * onPause\(\) : 사용자와 프래그먼트가 더 이상 상호작용하지 않게 되었을 때 호출된다.
  
`onStop()`

  * onStop\(\) : 프래그먼트가 사용자에게 더 이상 보이지 않게 되었을 때 호출된다.
  
`onDestroy()`

  * `onDestroyView()` : 뷰와 관련된 모든 리소스를 정리할 수 있는 기회를 프래그먼트에 제공한다.
  * `onDestroy()` : 프래그먼트는 자신이 생성한 모든 리소스를 정리할 수 있다.
  * `onDetach()` : 프래그먼트와 액티비티의 연결이 완전히 끊어질 때 호출된다.
