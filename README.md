# 문자열 덧셈 계산기

## 기능 목록

1. 사용자 입력 처리
    - [✅] 콘솔에서 사용자 입력을 받는 기능 구현
2. 문자열 파싱 기능
    - [✅] 기본 구분자 처리 - 쉼표, 콜론
    - [✅] 커스텀 구분자 감지 및 처리 - //와 \n 사이에 위치하는 문자 감지
3. 숫자 추출 및 변환
    - [✅] 추출된 문자열을 숫자로 변환
4. 덧셈 연산 기능
    - [✅] 변환된 숫자들의 합 계산
5. 결과 출력
    - [✅] 계산된 덧셈 결과를 콘솔에 출력
6. 예외 처리
    - [✅] 잘못된 입력에 대한 에러 메세지 생성 - `Error` 객체를 생성하고 `throw`

<br/>

## 예외 처리

1. 0이나 음수가 있는 경우 [✅]
2. 구분자로 모두 분리했을때 숫자가 아닌 값이 있는 경우 [✅]
3. 빈 입력을 한 경우 → “”의 경우 0으로 반환 [✅]

-   각 예외 상황에 대해 `[ERROR]`로 시작하는 에러 메세지를 제공하고 애플리케이션을 종료했습니다.

<br/>

## 테스트

1. 기본적인 기능
    - [✅] 공백 입력 (`“”` ⇒ 0)
    - [✅] 구분자가 없는 입력 (`1` ⇒ 1)
    - [✅] 공백이 포함된 입력 (`1, 2` ⇒ 3)
    - [✅] 숫자가 여러개 포함된 입력 (`1,2,3` ⇒ 6)
    - [✅] 2개의 구분자가 동시에 사용된 입력 (`1,2:3` ⇒ 6)
2. 커스텀 구분자 사용
    - [✅] 정상적으로 커스텀 구분자를 포함하여 작성한 입력 (`//;\n1;2;3` ⇒ 6)
3. 예외 처리
    - [✅] 숫자가 아닌 값을 포함
    - [✅] 0이나 음수가 포함
    - [✅] 잘못된 구분자
    - [✅] 커스텀 구분자 지정 형식이 잘못됨
