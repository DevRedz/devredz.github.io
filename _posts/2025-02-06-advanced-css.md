---
title: 스나이퍼팩토리 한컴AI - AI개발자 교육 5일차
description: advanced css (textbook CH6.5-7.2).
date: 2025-02-06 13:30:35 +09:00
categories: [web dev, css]
tags: [lecture,review]     # TAG names should always be lowercase
---

# CSS 복습
## `display` Property
```css
display: block | inline | inline-block | flex | none
```
### flex
- flex 는 기본적으로 가로정렬
- wa mark 웹접근성 인증
    - 접근성이 중요한 프로젝트 같은 경우에는 상속을 이용해 속성을 지정하기보다는 요소마다 지정을 해주는 것이 유리하다 예를 들면
> Ways to Hide Content
> `display: none;`
> `visibility: hidden;`
> `opacity: 0;`
> ⚠️ NOTE: `display: none;` takes no place
{: .prompt-tip }

## `position` Property
### Static (DEFAULT)
### Relative 
: relative to original static position 
- e.g. `left: 30px` 하면 원래 있어야하는 자리에서 좌로 30px 밀린다
- ⚠️ NOTE: doesn't affect anything else on screen

### Absolute
: relative to its CLOSEST parent element *Only and Only If* there's a parent element with position *other than* static.
⚠️ NOTE: unlike relative positioning, element get out of the flow of the doc. Meaning, other elements will take over its space. 

### Fixed
: fixed as users scroll the website


## Centering Element w/ CSS
- `text-align: center;`: center every child element that DOESN'T have a width set. 
- If it's a block (or inline-block), the child element need `margin: auto`

크몽에서 부업
웹디자인 파는 법
레이아웃에 대한 저작권

- css "초기화": 브라우저 세팅을 override 하기 위함
```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}
```

- `align-items: normal`이 기본 값이라 cross-axis 로 stretch 되서 꽉 차게 나온다. (`align-items: stretch`랑 뭐가 다른지 모르겠음). 


<br>
<footer>
본 후기는 [한글과컴퓨터x한국생산성본부x스나이퍼팩토리] 한컴 AI 아카데미 (B-log) 리뷰로 작성 되었습니다.
<br>
#한컴AI아카데미 #AI개발자 #AI개발자교육 #한글과컴퓨터 #한국생산성본부 #스나이퍼팩토리 #부트캠프 #AI전문가양성 #개발자교육 #개발자취업
</footer>