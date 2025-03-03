---
title: 스나이퍼팩토리 한컴AI - AI개발자 교육 1주차 회고
description: intro to js.
date: 2025-02-07 13:30:35 +09:00
categories: [web dev, css]
tags: [lecture,review]     # TAG names should always be lowercase
---


# JavaScript/TypeScript
- 마인크래프트 레드스톤 - 프로그램 안의 프로그램
- 구글 크롬이 생기고 구글이 웹이 더 빨라지게 만들기 위해 js를 해독하는 시스템을 아예 바꿈
- js 엔진을 구글이 오픈소스로 오픈하면서 생태계 확장
- server side: 는 node.js 가 발전됨
- react native 
- 웹 gpu 도 개발 - 웹에서 게임 가능
- tensorflow.js 로 머신러닝, 자연어 처리 응용, 이미지 인식 웹 앱 개발 등

## 컴파일 언어 vs. 인터프리터 언어
- 컴파일러로 변환이 이루어져야함
#### 동작과정
1. 컴파일러가 (소스어를) 기계어로 변환
2. 실행 파일 생성 (.exe .out)
3. 생성된 실행 파일 실행 

### 컴파일 언어 

#### 컴파일 언어의 장단점
+ 실행 속도가 매우 빠름
    + 기계어로 미리 변환되어 있음
+ 메모리 효율성이 높음
+ 보안성이 우수
    + 소스 코드 확인이 어려움

- 개발 과정이 복잡
- 컴파일 시간 필요
- 플랫폼 의존적: OS 별로 다른 컴파일 필요

### 인터프리터 언어 
: 매줄매줄 플랫폼 레벨에서 해석->실행 을 반복
: python, js, ruby

#### 인터프리터 언어의 장단점
+ 개발 속도가 빠름: 즉시 실행 및 결과 확인
+ 디버깅이 용이: 실시간 코드 수정/테스트
+ 플랫폼 독립적

- 소스 코드가 공개됨: 보안에 취약할 수 있음
    - 코드 난독화
    - react.js 압축

#### 하이브리드 방식: JIT 컴파일
- Java, C#에서 사용
- 실행 시점에 기계어로 컴파일
- 실행 속도와 개발 편의성 균형
- 플랫폼 독립성 유지

### JavaScript 생태계
#### 프레임워크와 라이브러리 
- React, Vue.js, Angular 등 인기 프레임워크
- 100만개 이상의 npm 패키지
- 웹팩, Babel 등 개발 도구

#### 서버 사이드 개발
- Node.js를 이용한 풀스택 개발
- Express.js 로 빠른 서버 구축
- MongoDB, MySQL 등 데이터베이스 연동

#### 테스트와 품질 관리
- Jest를 이용한 단위 테스트 작성
- Cypress 로 E2E 테스트 자동화
- ESLint 로 

## JS 개발환경
### 
- AI copilot: Github Copilot, Codisum, Windsurf

- head 에서 가져오는 것 vs body 에서 가져오는 것
    - 웹 브라우져에서 렌더링 전 / 후 에 불러오게 되는 차이
    - </body> 직전에 js script 을 불러와야 페이지가 로딩되는 속도가 빠르다

- js script 불러오는 방법 두가지
    - internal
    ```html
       <script>
        ...js code
    </script>
    ```
    - external
    ```html
    <script> src="script.js"</script>
    ```

    > html 에서 http*s* 등 보안서버로 지정했을 경우에 js script도 불러오는 src도 보안서버여야 한다; 아니면 js script가 보안이던 아니던 상관없다. 
    {: .prompt-warning }

    `<script> src="//script.js"</script>` 와 같이 http(s)를 생략하고 //로 대체함으로서 html 파일 보안 설정에 맞게 자동으로 다이나믹하게 설정 가능하다. 

    > 의존성이 있는 경우 js script 불러오는 순서 주의하기
    {: .prompt-warning }

## JS 문법
### JS 변수
#### 변수 이름 규칙
- special character는 `_`와 `$` 만 가능
- JS에서는 Camel case 선호, Python에서는 Snake case 선호

#### Initialize Variable 
- it's possible to define variable _w/o_ value.
1. `let`: variable value is changeable
2. `const`: non-changeable
3. `var`: `⚠️ obsolete ⚠️`

### Scope
>  함수 스코프, 지역 스코프 차이가 뭐지 
{: .prompt-danger }

### Hoisting
: 변수외 함수 선언이 코드의 맨 위로 "끌어올려지는" 것처럼 동작하는 자바스크립트의 특성 
: 실제로 코드가 이동하는 것은 아니며, 자바스크립트 엔진이 코드를 해석하는 방식
>  var가 hoisting 이 된다는거 안된다는 거 ?? 
{: .prompt-danger }

- 함수 호이스팅: 함수를 어디에서든지 define 해도 함수 실행 가능

#### `var` 키워드를 안쓰는 이유
`var`는 local scope 가 아닌 function scope로 읽힘.
따라서 scope 밖에서 access 해도 scope 안에서 지정된 값으로 보임 => 어떤 값으로 지정되었는지 파악 어려움

### ??
- ASI: 엔진이 자동적으로 `;` 를 붙혀줄 수 있지만 명시적으로 `;`를 사용하는 것이 안전함

## Data Type
### Types of Data
#### Primitive Type
: Value of the variable is directly saved
#### Reference Type
: Memory Adress that refers variable is saved
-e.g. object, array, function

<br>
<footer>
본 후기는 [한글과컴퓨터x한국생산성본부x스나이퍼팩토리] 한컴 AI 아카데미 (B-log) 리뷰로 작성 되었습니다.
<br>
#한컴AI아카데미 #AI개발자 #AI개발자교육 #한글과컴퓨터 #한국생산성본부 #스나이퍼팩토리 #부트캠프 #AI전문가양성 #개발자교육 #개발자취업
</footer>