---
title: 스나이퍼팩토리 한컴AI - AI개발자 교육 4일차
description: intro to css- css selecter, box model, properties (textbook CH4-5).
date: 2025-02-04 13:25:15 +09:00
categories: [web dev, css]
tags: [lecture,review]     # TAG names should always be lowercase
---

### box-sizing attribute
```css
box-sizing: border-box
``` 
```css
box-sizing: content-box
``` 
- `border-box`(DEFAULT):  width/height가 content 기준 설정 됨. border,margin,padding 은 설정사이즈 + ⍺
- `content-box`: border,margin,padding 이 포함된 기준으로 사이즈 설정 가능케 함. 

-inline block 도 좌우는 마진 설정 가능
-none, opacity, visibility 차이표 복습
-`overflow: hidden | scroll | auto | visible`

-css 에 넣을 때는 `<link>`->.html 에 넣는 것이 아닌 `@import`->.css 에 넣기
-class "resized" 로 설정하면 디폴트 폰트사이즈 (1 rem 단위도 바뀜)
    -`<html lang="en" class="resized">`  
-`oblique` 는 강제로 눕히는 거, `italic` 은 글꼴 지원될시에만 적용됨.
-`text-overflow: elipsis` 글자가 상자 넘어가면 ...으로 마무리

Q.DOM
<div class="A">
    <h1>
    <div class="B">
        <p>
.A {
    color: black;
}

### Resources 🪚
- Font Awesome (icon)

<br>
<footer>
본 후기는 [한글과컴퓨터x한국생산성본부x스나이퍼팩토리] 한컴 AI 아카데미 (B-log) 리뷰로 작성 되었습니다.
<br>
#한컴AI아카데미 #AI개발자 #AI개발자교육 #한글과컴퓨터 #한국생산성본부 #스나이퍼팩토리 #부트캠프 #AI전문가양성 #개발자교육 #개발자취업
</footer>
