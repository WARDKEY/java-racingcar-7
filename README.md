# java-racingcar-precourse

## 미션 2주차 - 자동차 경주

**초간단 자동차 경주 게임을 구현한다.**

## 기능 요구사항

1. 횟수가 주어지며 횟수 동안 n대의 자동차는 전진 또는 멈출 수 있다.

2. 각 자동차에는 이름이 부여된다. 전진하는 자동차 출력시 이름을 같이 출력한다.

3. 자동차 이름은 쉼표(,)를 기준으로 구분하며 이름은 5자 이하만 가능하다.

4. 몇 번의 이동을 할 것인지 사용자의 입력을 받는다.

5. 전진하는 조건은 0~9 중 무작위 값을 추출하여 4 이상일 경우 전진한다.

6. 게임 완료 후 우승자를 알려준다.(우승자는 1명 이상일 수동 있다.)

7. 우승자가 여려 명인 경우 쉼표(,)를 이용하여 구분한다.

8. 사용자가 잘못된 값을 입력한 경우 IllegarArgumentException을 발생시킨 후 애플리케이션은 종료되어야 한다.

## 기능 목록

### 1. 시작 문장 출력 기능
첫 줄에 "경주할 자동차 이름을 입력하세요.(이름은 쉼표(,) 기준으로 구분)"라는 문장을 출력한다.

### 2. 자동차 입력 기능
쉼표(,)를 기준으로 자동차 이름을 입력한다.

### 3. 시도 횟수 문장 출력 기능
"시도할 횟수는 몇 회인가요?"라는 문장을 출력한다.

### 4. 시도 횟수 입력 기능
사용자로부터 시도 횟수를 입력 받는다.

### 5. 부적절한 입력 판단 기능
입력이 잘못된 경우 예외를 터트린다.

### 6. 무작위 값 생성 기능
0~9 사이의 숫자 중에서 무작위 숫자 한 개를 생성한다.

### 7. 자동차 전진 조건 판단 기능
무작위 값 중 4 이상인 경우 전진한다.

### 8. 차수별 실행 결과 출력 기능
시도 횟수에 따른 각 차수별 실행 결과를 출력한다.

### 9. 우승자 출력 기능
최종 우승자를 출력한다.

## 에외처리
### - 이름 입력 시 이름을 입력하지 않은 경우
IllegalArgumentException("이름을 입력해 주세요.")을 터트린다.
### - 이름 입력 시 이름이 5자 이상인 경우
IllegalArgumentException("5자 미만의 이름을 입력해 주세요.")을 터트린다.
### - 이름 입력 시 쉼표(,)가 맨 앞에 있거나 맨 뒤에 존재하는 경우
IllegalArgumentException("쉼표(,)로 시작하거나 끝날 수 없습니다.")을 터트린다.
### - 시도 횟수로 음수가 입력된 경우
IllegalArgumentException("시도 횟수는 양수를 입력해주세요.")을 터트린다.
### - 시도 횟수로 숫자가 아닌 값이 입력된 경우
IllegalArgumentException("시도 횟수는 문자를 입력할 수 없습니다.")을 터트린다.
### - 시도 횟수로 0이 입력 된 경우
IllegalArgumentException("게임을 실행할 수 없습니다.")을 터트린다.
### - 시도 횟수로 1이 입력되었을 때 모든 차가 출발하지 않은 경우
IllegalArgumentException("전진한 차가 없어서 우승자가 없습니다.")을 터트린다.

## 사용 예제

**올바른 입력인 경우**
```
경주할 자동차 이름을 입력하세요.(이름은 쉼표(,) 기준으로 구분)
pobi,woni,jun
시도할 횟수는 몇 회인가요?
5

실행 결과
pobi : -
woni : 
jun : -

pobi : --
woni : -
jun : --

pobi : ---
woni : --
jun : ---

pobi : ----
woni : ---
jun : ----

pobi : -----
woni : ----
jun : -----

최종 우승자 : pobi, jun
```

**잘못된 입력인 경우**

```
경주할 자동차 이름을 입력하세요.(이름은 쉼표(,) 기준으로 구분)
pobi,woni,jun
시도할 횟수는 몇 회인가요?
-3

시도 횟수는 양수를 입력해주세요.
```
