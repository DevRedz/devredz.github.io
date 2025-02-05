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
-`overflow: hidden, scroll, auto, visible`