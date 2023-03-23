## 세미콜론
- console.log('Hello, world!');
- 세미콜론을 붙여도 붙이지 않아도 된다.
- 보통 통일성을 위해 모든 명령 뒤에 세미콜론을 붙인다.

## 주석 (comment)
- 사람이 알아볼 수 있도록 설명을 작성하는 부분
- //, /* ~~~ */

## 들여쓰기
- 보통 스페이스 2칸
- 코드의 가독성을 높여준다.
- if(condition) {
  - console.log('hello world');
- }

# 자료형 (dataType)
- 문자열
  - 표현식 (expression)
- 연산자
  - typeof

## 따옴표
- ' ', " ",
- 탬플릿 리터럴 (template literal) ` `

## 문자열 합치기
- 연산자이다.
- '긴 문자열도' + '하나로 합칠 수 있습니다'

### 숫자

## 숫자인지 확인하기
- typeof -> number(숫자)
- typeof NaN -> number

## 산술연산자
- +(더하기) -(빼기) *(곱하기) /(나누기) %(나머지) ** (지수)

## Infinity
- Infinity -> number
- -2/0 -> -Infinity
- Infinity - 100; -> Infinity
- Infinity - Infinity; -> NaN
- 0 / 0; NaN
- 형변환
  - 값의 자료형이 바뀌는 현상 또는 바꾸는 행위
- ex
  - '1' + 0; -> "10"  // 0이 숫자에서 문자열로 바뀌어서 더해진다.
  - "문자열" - 0; -> NaN // 문자열과 숫자가 만나면 NaN가 된다.
  - '9' - 5; -> 4 // 빼기는 문자가 숫자로 변환되어서 빼진다.

## 불 값
- true false
- != 는 양쪽 값이 다른지 비교하는 연산자.
- typeof true; -> "boolean"
- 5 > 3 -> true
- 5 < 3 -> ture
- 5 >= 3 -> true
- 5 <= 4; -> false
- 5 == 5; -> true
- 5 == 6; -> false
- 5 != 5; -> false
- 5 != 6; -> true
- NaN == NaN -> false // NaN끼리 비교하면 유일하게 false가 나옴
- true > false -> true // true는 숫자로 변환하면 1, false는 0
- '3' < 5; -> true // 빼기 연산자 처럼 숫자로 형변환 후 비교
- 'abc' < NaN -> false // 문자열은 NaN으로 변환
- '0' < true -> // 0이 숫자 0으로 형변환, true는 1

## == 와 === 차이
- '1' == 1; -> true
- 1 == true; -> true
- 1 == '1'; -> true

- ===는 자료형이 있는지 확인한다.
- '1' === 1; -> false
- 1 === true; -> false
- 1 === '1'; -> false
## 단항 연산자는 오른쪽에서 왼쪽으로 실행 ##

### 빈값 사용하기
- null
- undefined

- 공통점: 값이 없다
  - falsy value 취급
  - undefined == false
  - null == false
- 차이점:
  - 타입: null:object == undefined:undefined

- JS : undefined를 기본값으로 취급, 빈값표현은 undefined권장
  


## 2.3 변수 (Variable)
  - 변하는 수, 프로그램 실행시 임시로 저장하는 데이터 장소
  - 관례: 변수는 선언 및 초기화 후 사용하는 것 권장
### 1. 선언
  - const (constant)
    - 변하지 않는 수
    - const로 선언문을 사용할 경우 초기화 하지 않으면 에러
    - const로 선언한 상수에 값 쓰기 금지
  - let
    - 변할 수 있는 수
    - 선언문
  - var

* 변수명/상수명
  * $, _, 문자(유니코드😊, イヒョンミン, 로 가능), 숫자
  * 숫자로 시작할 수 없다.

* 선언만 하면 변수는 undefined;
  
### 2. 수정
  - let change = '이현민';
  - change = '2001492_이현민';

#### 값 초기화
  - change = nudefined;
  - change = null;
  
## 2.4 조건문
  - 주어진 조건에 따라 코드를 실행하거나 하지 않는 문
  - if (조건식) {실행문}
  
  - let condition = true;
  - if (condition) {console.log('Hello,if!');}
  - -> Hello,if!

  - if (0) {
    - console.log('Hello,if!);
    - }
## 별찍기 시험에 나올 수도 있음
### if 중첩문
  - 내포된 if
  - if 중첩문은 가독성이 떨어지기 때문에 가능하면 if-else if-else문으로 변환시키는 것이 좋다.
  
### switch 문
  - if 와 switch 공통점 : 조건이 충족되면 실행된다.
  - 차이점 : 조건식을 두개 사용, 실행문을 여러개 둘 수 있다.

  - 정의 방법
  - switch (조건식) {
    - case 비교 조건식 : 
      - 실행문;
  - }

#### 특징
  - if문의 else if 처럼 여러방향으로 분기할 수 있다. case를 여러번 사용하면 된다.
  - 일치하는 case 발견시 일치여부와 상관없이 아래 case를 모두 실행한다.
  - case에서 빠져나오려면 break문을 사용해야한다.
  - ex
  - let value = 'B';
  - switch (value) {
  - case 'A':
    - console.log('A');
  - case 'B';
    - console.log('B');
  - case 'C';
    - console.log('C');
    - break;
    - }

  - -> B C

  - default라는 예약어로 어떠한 case도 일치하지 않을경우 사용할 수 있다.
  - ex
  - switch (value) {
  - case 'A':
    - console.log('A');
    - break;
  - case 'B':
    - console.log('B');
    - break;
  - case 'C':
    - console.log('C');
    - break;
    - default:
    - console.log('아무것도 일치하지 않음');
  - }
  #### break문
  - 반복문에서도 사용
    - block : { ~ } 형태의 코드
  - 실행 block 중단하는 코드
  - 실행의 범위
    - break문이 속해 있는 block 하나만 중단
    - for(){ for(){ break }}
  - break 뒤에는 break를 붙이지 않아도 된다.
  - break는 어디에 둬도 상관없다.
  #### continue문
  - 중단
  - continue문이 실행되면 조건문 검사를 실행함
  

### 조건부 연산자 사용하기
  - 조건부 연산자 or 삼항 연산자 : if 문과 switch 문 외에도 분기 처리에 사용하는 식
  - 정의 방법
  - 조건식 ? 참일 때 실행되는 식 : 거짓일 때 실행되는 식
  - ex
  - 5 > 0 ? '참입니다' : '거짓입니다'
  - -> 참입니다

  - condition ? condition2 ? '둘 다 참' : 'condition1만 참' : 'condition1이 거짓';

## 2.5 반복문
### while
  - 조건식이 만족하는 동안(true인 동안) 블록내의 문장 실행
  - 조건식을 만족시킬 수 있는 문장; // (1)
  - while (조건식) { // (2)
  -  실행문1;
  -  실행문2;
  -  실행문3; 
  -  맨 마지막 조건식의 값 변화에 영향을 끼치는 문장; // (3)
  - }

while (조건식) {
  실행문

  let i ++;
}

### do while
- do 일단 한번 시작한다.
- do{
  - 문장들;
    - ...
  - 맨마지막 조건식의 값 변화에 영향을 끼치는 문장;
- }while(조건식);

### for
  - for문 정의 방법
  - for((1)초기식; (2)(5)(8)조건식; (4)(7)변화식) {
  - (3)(6)실행문;
  - }

  - 초기식(1)
  - 조건식(2)
  - 변화식(3)

  - continue 넣으면 반복문을 그만두고 나올수 있다.

#### 중첩 반복문
  - 반복문 안에 반복문이 있는 경우
  - 이중 반복문, 삼중 반복문
  - for (let i = 0; i < 10; i++) {
    - for(let i = 0; i < 10; i++)
      
      
       console.log(i, j);
    - }

  0 0
  0 1
  0 2
  ---
  9 7
  9 8
  9 9
  
  - quiz
   for(let i = 0; i < 10; i++) {
  for(let j = 0; j < 10; j++) {
    if(i % 2 === 0 || j % 2 === 0) continue;
      console.log(i*j);
    }
  }

## 2.6 객체 (object)
  - JS 데이터타입의 일종
  - 배열, 함수, 그 외 정의해나가는 자료(객체)

### 배열 (array)
- 나열할 수 있는 데이터를 집합적으로 관리할 수 있는 데이터 타입
- 나열가능한 데이터
  - 배열, 객체, primitive type, null, undefined, Infinity, NaN
- 데이터의 중복 가능, 순서 상관없음
- 요소 : element, 배열의 저장되는 하나의 데이터
- 인덱스(index): 특정한 요소의 저장위치

#### 1. 선언 / 정의
- 대괄호 사용: [요소1, 요소2, ...]
- Array() 사용: Array객체의 생성자
  - new Array(숫자): 빈 배열을 숫자만큼 생성
  - new Array(요소1, 요소2, ...)
- 배열내에 배열요소가 저장되도록 한 것: 다중배열(다차원배열), 이중배열(이차원배열)

#### 2. 사용
- 배열의 크기(길이): 배열명.length
  - 맨마지막 요소의 인덱스: 배열명.length-1
- 읽기
  - 배열명[인덱스]
- 쓰기
  - 배열명[인덱스] = 쓸값
- 수정
  - 배열명[인덱스] = 수정 값
- 삭제
  - delelte 배열명[인덱스]
  - 해당요소 empty
- 추가
- 맨 마지막에 추가
  - 배열명[배열명.length] = 추가값
  - 배열명.push(추가값)

- 맨 앞에 추가
  - 배열명.unshift(추가값)
- 맨 마지막 꺼 삭제
- 배열명.pop(): 삭제한 요소를 반환
- 맨 앞 꺼 삭제
- 배열명.shift(): 삭제한 요소를 반환
- 수정과 삭제
- 배열명.splice(시작index, [삭제요소갯수,[추가할 요소]])
- 배열명.splice(시작index) 
  - 시작 index에서 배열 끝까지 삭제
- 배열명.splice(시작, index, 시작요소갯수, 추가할 요소들)
  - 시작index에서 지정한 갯수만큼 삭제하고,추가요소 삽입
- 검색
- 배열명.includes(검색할 요소)
  - 반환값: boolean
- 배열명.indexOf(검색할 요소)
  - 반환값: index값
  - 맨처음부터 검색하여 검색성공한 최초의 인덱스
  - 못찾으면 -1 반환
- 배열명.lastIndexOf(검색할 요소)
  - 반환값: index값
  - 맨마지막부터 검색하여 검색성공한 최초의 인덱스
  - 못찾으면  -1 반환
- 반복
  - for문사용
  - for~in문사용
  - 배열명.forEach(함수)

### 함수(function)
- 특정한 작업을 수행하는 코드들의 집합
- 비유: 자판기
  
#### 1. 정의 / 선언
- 선언문
  - function 함수명(parameter list) { // 함수의 시그니쳐, 함수의 헤더
    // 중괄호 부분 : 함수의 바디
  }
- 표현식 (expression) : 연산자 (=)
  - 이름없는 선언문
    - const 상수명 = function(parameter list) {}; // 호출 : 상수명(argument list)
  - 화살표 함수(Arrow Function)
    - const 상수명 = (parameter list) => {};
  - 화살표 함수의 this 와 function 함수의 this는 다르다.
#### 2. 호출
- 함수명(argument list)
- 상수명(argument list)
- 호출하면 반드시 결과를 반환함
  
#### 3. parameter / argument
- parameter : 가인수
  - 함수선언시 함수 시그니쳐에 나오는 인수
- argument : 실인수
  - 함수호출시 사용하는 인수
#### 4. return
- return 데이터(변수, 리터널);
- return을 명시하지 않은 경우 return undefined; 맨마지막 실행
  - 함수 내부에서 return 문을 실행하는 경우 함수 실행 중지
  - 함수 호출한 곳으로 실행순서 이동
#### 5. 함수내의 사용 변수 : scope
- 전역변수: 함수내외부에서 사용가능
- 지역변수: 함수내에서만 사용 가능
- 파라미터: 지역변수 취급

#### 순수함수
- 파라미터와 지역변수/상수만으로 구현한 함수

#### 함수선언과 화살표함수 비교
- function add1(x, y) { return x+y;}
- const add2 = function(x, y) { return x+y;};
- const add3 = (x,y) => { return x+y;};
- const add4 = (x,y) => x+y; // 함수 실행문이 return만 존재하는 경우 중괄호 + return 생략가능
- const not = x => !x; // 파라미터가 하나인 경우 소괄호 생략가능 not(test)
- 주의사항: this의 의미