## 전역 변수의 문제점

변수는 생성되고 소멸되는 생명주기가 존재

함수 내부에서 선언된 지역변수는 함수가 호출되면 생성되고 함수가 종료되면 소멸한다.

지역 변수의 생명주기는 함수의 생명주기와 일치한다.

변수의 생명주기는 메모리 공간이 확보된 시점부터 메모리 공간이 해제되어 가용 메모리 풀에

반환되는 시점까지다.

함수 내부에서 선언된 지역변수는 함수가 생성한 스코프에 등록된다.

함수가 생성한 스코프는 렉시컬 환경이라 부르는 물리적 실체가 존재한다.

변수는 자신이 등록된 스코프가 소멸될 때까지 유효하다.

스코프도 마찬가지로, 어떤 대상이 참조하고 있으면 스코프는 소멸하지 않는다.

호이스팅은 스코프 단위로 동작한다.

var 키워드로 선언한 전역변수는 전역 객체의 프로퍼티가 된다.

→ 전역 변수의 생명주기가 전역객체의 생명주기와 일치한다는 것을 말한다.

### 전역 변수를 선언한 의도

모든 코드가 전역변수를 참조하고 변경할 수 있는 암묵적 결합을 허용하는 것

→ 변수의 유효 범위가 클수록 가독성은 나빠지고 상태가 변경될 수 있는 위험성도 높아진다.

전역변수는 생명주기가 길며, 메모리 리소스도 오랜 기간동안 소비한다.

전역변수는 스코프 체인 상에서 종점에 존재한다.

즉, 전역 변수의 검색 속도가 가장 느리다.

### 자바스크립트의 가장 큰 문제점

파일이 분리되어 있다 하더라도, 하나의 전역 스코프를 공유한다는 것이다.

변수의 스코프는 좁을수록 좋다.

### 전역변수 사용 억제 방법

1. 즉시 실행함수 - 라이브러리 등에 자주 사용된다
2. 네임스페이스 객체
3. 모듈 패턴 
    
    -클로저를 기반으로 동작한다.
    
    -전역 변수 억제 및 캡슐화 구현 가능
    
4. ES6 모듈
    
    -파일 자체의 독자적인 모듈 스코프를 제공한다.
    
    -전역 변수를 사용할 수 없다.