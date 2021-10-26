# Thymeleaf
- 서버 사이드 HTML 렌더링(SSR)
- 네츄럴 템플릿
  - 순수 HTML 최대한 유지 + View Template 사용 가능
- 스프링 통합 지원

사용 선언
````html
<html xmlns:th="http://www.thymeleaf.org">
````

### 기본 표현식
- 간단한 표현:
  - 변수 표현식: ${...}
  - 선택 변수 표현식: *{...}
  - 메시지 표현식: #{...}
  - 링크 URL 표현식: @{...}
  - 조각 표현식: ~{...}
- 리터럴
  - 텍스트: 'one text', 'Another one!',…
  - 숫자: 0, 34, 3.0, 12.3,…
  - 불린: true, false
  - 널: null
  - 리터럴 토큰: one, sometext, main,…
- 문자 연산:
  - 문자 합치기: +
  - 리터럴 대체: |The name is ${name}|
- 산술 연산:
  - Binary operators: +, -, *, /, %
  - Minus sign (unary operator): -
- 불린 연산:
  - Binary operators: and, or
  - Boolean negation (unary operator): !, not
- 비교와 동등:
  - 비교: >, <, >=, <= (gt, lt, ge, le)
  - 동등 연산: ==, != (eq, ne)
- 조건 연산:
  - If-then: (if) ? (then)
  - If-then-else: (if) ? (then) : (else)
  - Default: (value) ?: (defaultvalue)
- 특별한 토큰:
  - No-Operation: _

### 기본 객체들
- ${#request}
- ${#response}
- ${#session}
- ${#servletContext}
- ${#locale}

### 문자 리터럴
- 문자 리터럴은 항상 '(작은 따옴표)로 감싸야 함 (단, 공백 없이 이어진다면 생략 가능)
````html
<span th:text="'hello'">
````