---
title: 스나이퍼팩토리 한컴AI - AI개발자 교육 2일차
date: 2025-02-03 14:22:15 +09:00
categories: [web dev, html]
tags: [lecture,review]     # TAG names should always be lowercase
---
Table of Contents
1. [HTML 기본 구성 요소](#-html-기본-구성-요소)
2. [HTML 기본 구조](#-html-기본-구조)
3. [HTML 특징](#-html-특징)
4. [HTML 태그](#-html-태그)

## ❶ HTML 기본 구성 요소
1. 태그
2. 속성 (attribute)
3. 문법
4. 주석 `<!--주석-->`

## ❷ HTML 기본 구조
```html
<!DOCTYPE html> <!--문서형 정의 DTD-->
<html lang="en">
<head> <!--문서의 메타 데이터를 정의해주는 영역-->
    <meta charset="UTF-8"> <!--언어 설정-->
    <meta http-equiv="X-UA-Compatible" content="IE=edge'> <!--인터넷 렌더링 엔진 지정-->
    <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
    <title></title> <!--웹 사이트에서 제목이 중복된 문서를 만들지 않기-->
</head>
<body>
</body>
</html>
```

## ❸ HTML 특징
### block element & inline element
block element
  : 공간 유무와 상관없이 사용할 때 마다 줄 바꿈되는 태그
  : e.g. `h1`, `p`
inline element
  : e.g. `a`, `span`

## ❹ HTML 태그
### 🅐 텍스트 작성 태그
#### h _n_
---
`<h1></h1>`
- 검색 엔진에서 키워드로 인식됨. 검색 엔진 최적화 (SEO) 를 위해 신중히 작성.

#### p
---
`<p></p>`

#### br 
---
`<br>`: 줄바꿈

#### blockquote
---
`<blockquote cite="source URL"><p>문단 단위 인용문</p></blockquote>`
- `cite` attribute은 옵션
- 무조건 1개 이상 'p' tag 포함해야함

#### q
---
`<q cite="source URL">짧은 인용문</q>`

#### ins & del
---
`<ins>추가 텍스트</ins>` 와 `<del>삭제 텍스트</del>`

#### sub & sup
---
`<sub>아래 첨자</sub>` 과 `<sup>위 첨자</sup>`

### 🅑 그룹 태그
  :관련 있는 요소끼리 그룹 짓는 태그들

#### div
---
`<div>inline elements and block elements</div>`
#### span
---
`<span>inline elements</span>`

### 🅒 목록 태그
#### unorderly list
#### orderly list
#### description list

### 🅓 링크와 이미지
#### a
---
`<a href="대상 경로" target= "링크 연결 방식" title="링크 설명">링크가 표시되는 글</a>`
-`href`는 필수 나머지는 선택. 혹 href 값이 아직 없다면 `#`입력
-`target`은 새 창으로 열리는 방식인 `_blank`값을 제외하고 거의 생략
-`title`은 `a`tag의 콘텐츠 만으로 표현하지 못한 링크 설명

#### img
---
`<img src="이미지 경로" alt="이미지 설명">`
- `src`와 `alt`모두 필수
- `../`는 상위 폴더 `./`는 현재 폴더; e.g. `../../imgs/beach.jpg`
- 이미지를 링크로 쓰고 싶다면 nest `img` tag inside `a` tag
  
### 🅔 텍스트 강조

#### strong
---
- 중첩 가능 (강조 효과는 동일 but 코드 읽는 사람이 구조적으로 강세를 파악하기 위함)

#### em
---
- 기울임 & 강조
- 중첩 가능 just like `strong`

### 🅕 폼 구성하기
#### form
---
`<form action="server url" method="get OR post"></form>`
- action : form element 에서 사용자와 상호작용으로 입력받은 값들을 전송할 서버의 URL 주소
- method : 서버에 전송할 때 송신 방식
- 
#### input
---
`<input type="" name="" value=""></input>`
![input tag type attribute list](https://www.codewithfaraz.com/img/Understanding%20the%20HTML%20Input%20Tag%20and%20Its%20Types.jpg)
- name: 입력 요소가 form tag에 의해 서버로 전송될 때, name 속성에 적힌 값이 이름으로 지정됨.
- value: 입력 요소의 디폴트 값

#### label
---
태그 안에서 사용하는 상호작용 요소에 이름을 붙일 때 사용; 웹 접근성을 높이기 위해 필요함

##### 암묵적 사용
```html
<label>
  아이디
  <input type="text">
</label>
```

##### 명시적 사용
```html
<label for="userpw">비밀번호</label>
<input type="password" id="userpw">
```

##### 함께 사용
```html
<label for="userpw">
비밀번호
<input type="password" id="userpw">
</label>
```

#### fieldset & legend
---
- fieldset: form tag 안에 사용된 여러 상호작용 요소를 *그룹* 지음
- legend: 그룹에 이름 붙임

```html
<form action="#">
  <fieldset>
    <legend>그룹 이름</legend>
  </fieldset>
</form>
```

#### textarea
---
`<textarea>초깃값</textarea>`
여러 줄의 input text를 받을 때 `input` tag 대신 사용

#### select & option & optgroup
---
- option tag는 서버에 전송할 값을 value attribute으로 지정가능. 단 attribute을 생략하면 option tag 의 contents로 적은 text가 전송됨.
- optgroup tag로 항목들을 그룹 지을 때 반드시 label attribute 으로 그룹명을 지정해야함

```html
<select name="fruits" size="3" multiple>
  <optgroup label="과일">
    <option value="apple" selected>사과</option>
    <option value="banana">바나나</option>
    <option value="grape">포도</option>
  </optgroup>
  <optgroup label="채소">
    <option value="carrot">당근</option>
    <option value="spinach">시금치</option>
    <option value="potato">감자</option>
  </optgroup>
</select>
```
- size attribute: 콤보박스에서 화면에 노출되는 항목 개수 (미설정시 기본으로 1개 항목 표시)
- multiple attribute: 여러 항목 동시에 설정
- selected attribute: 기본 선택 항목

#### button
---
- input tag에서 type attribute 값을 submit, reset, button으로 지정해 생성 가능
- 별도의 button tag도 가능
`<button type="">버튼내용</button>`
- 이미지를 nested 해서 많이 쓴다.
- type attribute 속성값
  - submit: 폼을 서버에 전송
  - reset: 입력 내용 초기화
  - button: 단순한 버튼
  
#### 그 외 form 관련 tag에서 사용할 수 있는 추가 _attribute_
---
- `disabled`
- `readonly`
- `maxlength`
- `checked`
- `placeholder`

### 🅖 표 만들기
#### table
---
```html
<table>
  <tr>
    <th></th>
    <th></th>
  </tr>
  <tr>
    <td></td>
    <td></td>
  </tr>
</table>
```

#### caption
---
#### tr, th, td
---
#### rowspan & colspan _attribute_
---
- merge 하려는 td 들 중 첫 번째 td에 적용. 병합한 셀 개수만큼 다음 셀은 비워야한다.

#### thead, tfoot, tbody 
---
- 보통 청각접근성을 위해 씀
- grouping rows
- must be in order: thead, tfoot, tbody

#### col & colgroup 
---
- grouping cols
- 보통 스타일링을 위해 씀
- caption 태그 뒤, tr 태그 전에 사용해야 함

#### scope _attribute_
---

### 🅗 멀티미디어 설정하기
- browser 마다 오디오/video 파일 포맷이 다르다.
#### audio
---
- MP3 -> mpeg / WAV -> wav / OGG -> ogg

```html
<audio 
  src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" 
  controls <!--웹 브라우저에 노출-->
  autoplay
  loop 
  muted>
  브라우저가 오디오 태그를 지원하지 않는 경우 이 텍스트가 표시됩니다.
</audio>
```

#### video
---
- MP4 -> mp4 / WAV -> webm / OGG -> ogg

```html
<video 
  src="https://www.w3schools.com/html/mov_bbb.mp4" 
  controls 
  autoplay 
  loop 
  muted 
  preload="auto" 
  poster="https://www.w3schools.com/html/pic_trulli.jpg" 
  width="640" 
  height="360">
  브라우저가 비디오 태그를 지원하지 않는 경우 이 텍스트가 표시됩니다.
</video>
```

#### source
---
- 보통 웹브라우저에서 내가 원하는 포맷의 미디어 타입을 지원하지 않을 때 쓴다. 웹브라우저는 그 다음 source를 차례대로 확인한다. 아무 source도 재생할 수 없다면 마지막으로 텍스트를 노출.

```html
<audio controls>
  <source src="sample.wav' type="audio/wav">
  <source src="sample.mp3' type="audio/mp3">
  지원하지 않는 웹 브라우저입니다.
</audio>
```

### 🅘

### 🅙


본 후기는 [한글과컴퓨터x한국생산성본부x스나이퍼팩토리] 한컴 AI 아카데미 (B-log) 리뷰로 작성 되었습니다.

#한컴AI아카데미 #AI개발자 #AI개발자교육 #한글과컴퓨터 #한국생산성본부 #스나이퍼팩토리 #부트캠프 #AI전문가양성 #개발자교육 #개발자취업
