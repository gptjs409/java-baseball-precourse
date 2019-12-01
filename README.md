# 기능 요구 사항

### main 메서드

게임 시작

- String makeAnswer()로 정답 생성

- String inputNumbers()로 숫자 받아옴

- boolean checkedNumbers()로 숫자 확인함

  - 맞으면 게임 종료
  
  - 틀리면 inputNumbers()부터 다시

- boolean restart()로 다시 시작 여부 확인

  - 1을 입력시 재시작
  
  - 2를 입력시 종료

<br>

### String makeAnswer() 메서드

처리

- 1 ~ 9까지 서로 다른 임의의 수 3자리를 생성

  - 예) 123, 456, 789

리턴값

- 생성값 반환


<br>

### String inputNumbers() 메서드

처리 

- 출력값 : 숫자를 입력해주세요 : (입력받기)

- 입력은 Scanner로

  - 1 ~ 9까지 서로 다른 수로 이뤄진 3자리 수

  - 세 자리 수가 아니거나 세 자리 수 중 같은 숫자가 있다면 다시 입력할 수 있도록 가이드
  <br>"1 ~ 9까지 서로 다른 수로 이뤄진 3자리 수로 입력해주세요 : "

<br>

### boolean checkedNumbers(String numbers, String answer) 메서드

처리 

- 출력형식 : \[n 스트라이크] \[n볼] | \[낫싱] 

- numbers 값과 answer 값을 비교(자리별로)

  - 같은 수가 같은 자리에 있다면 (n)스트라이크

  - 같은 수가 다른 자리에 있다면 (n)볼

  - 같은 수가 전혀 없다면 포볼 or 낫싱

- 다 맞출 경우 (3 스트라이크)

  - 출력값 : 3개의 숫자를 모두 맞히셨습니다! 게임 종료

리턴값

- 다 맞춘 경우 false

- 다 맞추지 못한 경우 true

<br>

### boolean restart() 메서드

처리

- 출력값 : 게임을 새로 시작하려면 1, 종료하려면 2를 입력하세요.

- Scanner로 사용자로부터 값을 입력받기

  - 만약 이상한거 입력하면? 다시 재출력
  
  - 종료시엔 "수고하셨습니다."를 띄워줘보자. 

리턴

- 1을 입력받았을 경우 : true

- 2를 입력받았을 경우 : false 