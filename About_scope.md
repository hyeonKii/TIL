## 스코프

함수를 배웠을 때 이미 스코프를 경험했다.

함수의 매개 변수의 경우, 함수 몸체 내부에서만 참조할 수 있고, 외부에서는 참조할 수 없다.

즉, 매개변수의 스코프가 함수 몸체 내부로 한정되어 있기 때문이다.   

모든 식별자는 자신이 선언된 위치에 의해 다른 코드가 식별자 자신을 참조할 수 있는 유효 범위가 결정된다.

즉 스코프는 식별자가 유효한 범위를 뜻한다.

### 식별자 결정

자바스크립트 엔진이 이름이 같은 두개의 변수 중에서 어떤 변수를 참조할 것인지 결정하는 것

전역에서 선언된 변수 = 전역 스코프를 갖는다

지역에서 선언된 변수 = 지역 스코프를 갖는다

전역 변수는 어디서든 참조할 수 있다

지역 변수는 자신의 지역 스코프가 하위 지역 스코프에서 유효하다

함수 몸체 내부에서 정의한 함수를 중첩함수라 한다.

중첩 함수를 포함하는 함수를 외부 함수라 한다.

### 스코프 체인

모든 지역 스코프의 최상위 스코프는 전역 스코프다.

스코프가 계층적으로 연결된 것을 스코프 체인이라고 한다.

스코프 체인은 물리적으로 존재한다.

자사스크립트 엔진은 코드를 실행하기 전에 렉시컬 환경을 실제로 생성한다. 변수 선언이 실행되면

변수 식별자가 렉시컬 환경의 키로 등록되고, 변수 할당이 일어나면 변수 식별자에 해당하는 값을 변경한다.

*전역 렉시컬 환경은 코드가 로드되면 바로 생성되고, 함수 렉시컬 환경은 함수가 호출되면 곧바로 생성된다.

하위 스코프에서 유효한 변수를 상위 스코프에서 참조할 수 없다.

스코프 체인에 의한 함수 검색

함수 선언문은 런타임 이전에 함수 객체가 먼저 생성된다.

자바스크립트 엔진은 함수 이름과 동일한 식별자를 암묵적으로 선언하고 생성된 함수 객체를 할당한다.

함수도 식별자에 할당되기 때문에 스코프를 갖는다.

### 함수 레벨 스코프

코드블록이 아닌 함수에 의해서만 지역 스코프가 생성된다.

var 키워드로 선언된 변수는 오로지 함수의 코드 블록만 지역 스코프로 인정한다.

### 블록 레벨 스코프

모든 코드 블록이 지역 스코프를 만든다.

### 동적 스코프

함수를 어디서 호출했는지에 따라 함수의 상위 스코프를 결정한다.

### 렉시컬 스코프

함수를 어디서 정의했는지에 따라 함수의 상위 스코프를 결정한다.

자바스크립트는 렉시컬 스코프를 따른다.

함수의 상위 스코프는 언제나 자신이 정의된 스코프다.

함수 정의(함수 선언문, 함수 표현식)가 실행되어 생성된 함수 객체는 상위 스코프를 기억한다.

함수가 호출될 때마다 함수의 상위 스코프를 참조할 필요가 있기 때문이다.