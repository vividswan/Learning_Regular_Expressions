# Chapter 02 - 문장 하나 찾기

## 문자 그대로 찾기

- 평범한 텍스트도 정규 표현식이 될 수 있다.
  - 평범한 텍스트를 `정적 텍스트(static text)`라고 부른다.

### 얼마나 많이 일치하는가?

- 대다수 정규 표현식 엔진은 가장 처음 일치한 텍스트를 반환
  - 또한 일치하는 목록을 모두 얻을 수도 있음 (배열이나 다른 특별한 형태로 반환, ex) 자바스크립트의 g 플래그)

### 대소문자 다루기

- 정규 표현식에서는 대소문자를 구별
- 대소문자 구별을 무시하는 기능도 대다수 존재
  - ex) 자바스크립트의 i 플래그

## 모든 문자 찾기

- 정규 표현식에서는 특별한 문자들이나 문자 집합을 사용해 무엇을 검색할지 결정
- 마침표(.) 문자는 아무 문자 하나와 일치
  - 어떠한 문자나 알파벳, 숫자, 문장 부호로 쓰인 마침표 자체와도 일치
  - ex) c.t를 검색 시 cat, cot을 비롯한 단어들과 일치
  - 여러 개를 동시에 사용할 수 있음 (.. => 붙어 있는 문자 두 개와 일치)
  - 대다수 정규 표현식 구현에서 마침표는 줄바꿈 문자를 제외한 모든 문자와 일치

## 특수문자 찾기

- 정규 표현식에게 특별한 의미의 마침표(.)가 아닌 진짜 마침표(.)를 찾을 땐 마침표 앞에 역슬래시 문자를 붙이기
- 역슬래시는 `메타 문자`
  - 메타 문자는 일반적으로 문자 그대로 사용되지 않고 특별한 의미를 지니는 문자를 칭함
  - 정규 표현식에선 주로 특별한 의미를 지니는 문자의 맨 앞에 표시 (이런 문자는 한 글자 이상인 경우도 존재)
  - 역슬래시 자체를 찾고 싶을 땐 "\\\\"
