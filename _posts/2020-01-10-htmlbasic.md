---
layout: post
title: "[HTML] HTML 기초"
tags: HTML
---

* *문서의 구조와 정보 위계가 명확하게 보이는 아름다운 html 코드를 작성하자.*
* **시맨틱 마크다운**
* 개발자도구 단축키는 손에 익히도록 하자. -> `option` + `command` + `I`
* `command` + `shift` + `p` -> vscode 스팟라이트
```
<strong></strong> <!-- 강조 -->
```
```
<br/> <!-- break의 약자. 줄바꿈. -->
```
* `href`는 hypertext reference의 줄임말이다.
* `<a href = "상대경로 or 절대경로">`
* `<section id="hello">`가 있고, 한 페이지 안에서 섹션으로 이동하고 싶다면, `<a href = "#hello">`를 사용하면 가능하다.
* `target="_blank"`를 쓰면 새 탭을 여는 방식으로 새 페이지를 열 수 있다.

```
<img src = "#" alt = "" />
```
* `src`는 source의 약자이고 (이미지의 링크)
* `alt`는 alternative text의 약자 (대체 텍스트, 이미지에 대한 설명 텍스트)
## ul과 ol

```
  <ul>
    <li>항목1</li>
    <li>항목2</li>
    <li>항목3</li>
  </ul>
```
* ol(ordered list)는 순서가 중요한 목록
* ul(unordered list)
* li(list item)
* ul의 자식요소는 필수적으로 `<li>`만 가능하다.
## dl(discription list)

```
<dl>
  <dt>학습</dt> <!-- discription term -->
  <dd>배워서 익히는 일</dd> <!-- discription data -->
</dl>
```

* dl의 자식요소로는 오직 `div`, `dt`, `dd`만 가능하다.
## form
사용자로부터 인풋을 받기 위한 태그
```
<form action="" method=""></form>
```
* `action`은 API주소 : 이걸 처리해 줄 API 서버 쪽 친구에게 접근이 가능한 URL이다.
* `method`는 GET과 POST.
## input
```
<input type="text"/>
```
```
<input type="text" placeholder="이름을 입력하세요." 
    maxlength="13" minlength="5" value="finn" />  
```
* `placeholder`는 힌트
* `maxlength` 를 넘지 않고, `minlength`보다 많은 글자를 입력해야 한다.
* `value`는 초기값
### 특별한 input type
#### file
```
<input type = "file" accept= ".png,.jpg"/>
```
* 파일을 첨부하는 input을 만들고 싶을 때 사용.
* 확장자를 제한하고 싶을 때는 `accept` 속성에 value로 제한할 확장자를 추가한다.
#### radio
```
<form action="#" method="GET">
  <input type="radio" name="subscription" id="subscribed" value="subscribed"/>
  <label>구독중</label>
  <input type="radio" name="subscription" id="unsubscribed " value="unsubscribed"/>
  <label>미구독</label>
  <button>
    전송
  </button>
</form>
```
* 여러 개의 radiobutton이 있어도 체크값이 중복되지 않게 해야 한다.
* (실제 radio버튼은 하나를 누르면 하나가 튕겨져 나온다.)
* 여러 개의 radiobutton은 같은 name속성으로 묶인다.
* value 속성은 무조건 필요하다.
![](https://images.velog.io/images/star146913/post/17238381-5a02-49be-8f01-b595cfa543c7/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-02-09%2019.34.48.png)
* button을 누르면 GET방식으로 submit하게 되어 있다.
* radiobutton이 구독에 체크되어 있으면
![](https://images.velog.io/images/star146913/post/6afb7180-3c24-452c-86d5-5b121f43deda/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-02-09%2019.35.04.png)
* 미구독에 체크되어 있으면
![](https://images.velog.io/images/star146913/post/36a6d5da-9556-40ce-a430-0d4d456c77dc/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-02-09%2019.37.08.png)
* 각각 다른 value 속성을 넘겨주는 것을 확인할 수가 있다.
#### checkbox
```
<form action="#" method="GET">
    <input type="checkbox" name="skills" value="html"/>
    <label for="html">html</label>
    <input type="checkbox" name="skills" value="css"/>
    <label for="html">css</label>
    <input type="checkbox" name="skills" value="js"/>
    <label for="html">js</label>
    <button type="submit">
      submit
    </button>
 </form>
```
* 모든 체크박스에 체크가 되어 있는 상태에서 `submit` button을 누를 시에
![](https://images.velog.io/images/star146913/post/a2a1ba42-8f9a-4f65-8a7c-0773b175fe74/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-02-15%2007.27.11.png)
* `name=value`의 형태

## label
```
<label for = "user-name">이름</label>
<input type = "text" id = "user-name"/>
```
* input의 명칭을 정해준다.
* 다음과 같이 표시된다.

![](https://images.velog.io/images/star146913/post/febab38b-21b7-436b-a4db-a5fe5d5e2554/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-02-09%2018.35.42.png)

## select
```
<label for="skill">skill</label>
<select name="skill" id="skill">
  <option value="html">HTML</option>
  <option value="css">CSS</option>
  <option value="js">JS</option>
</select>
```
* select에서 `name`은 `option`을 위한 것, `id`는 `label`을 위한 것.

## textarea
```
<textarea cols="10" rows="10"></textarea>
```

## button
```
<button type="button">버튼</button>
<button type="submit">제출</button>
<button type="reset">다시 쓰기</button>
```

## table
```
<table>
  <tr> <!-- 가로줄 만들거야 -->
    <th>테이블 헤더</th>
    <td>테이블 데이터</td>
  </tr>
</table>
```
* 가로줄을 기준으로 생각한다. 행에 셀을 옆으로 쌓는다고 생각하자.
```
<table>
    <thead>
      <tr>
        <th>ID</th>
        <th>이름</th>
        <th>개발분야</th>
        <th>기타</th> 
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>00001</td>
        <td>황예지</td>
        <td>프론트엔드</td>
        <td></td> <!--데이터가 없더라도 헤더에 맞게 셀을 만들어주어야 한다.-->
      </tr>
      <tr>
        <td>00002</td>
        <td>최지수</td>
        <td>백엔드</td>
        <td></td>
      </tr>
    </tbody>
</table>
```
* `lowspan`은 행 병합, `colspan`은 열 병합
* 가로줄에 헤더가 있을 수 있고, 세로줄에 해더가 있을 수 있다. 그것을 좀 더 명시적으로 나타내주기 위해서, 가로줄에 대한 헤더는 `<th scope="col">`을, 세로줄에 대한 헤더는 `<th scope="row">`를 써준다.

