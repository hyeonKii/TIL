### 명시적 타입 변환(explict_coericon)
=타입 캐스팅(type casting)   
> 개발자가 의도적으로 값의 타입을 변환하는 것


### 암묵적 타입 변환(implicit_coericon)
=타입 강제 변환(type coericon)   
> 자바스크립트 엔진에 의해 암묵적으로 타입이 자동으로 변환되는 것

ex)   
var x = 10;   
var str = x + '';

console.log(typeof str, str); // string 10   
console.log(typeof x, x); // number 10

명시적 타입 변환과 암묵적 타입 변환이 기존 원시 값을 직접 변경하지 않는다.   
원시 값은 immutable value이므로 변경할 수 없다.   
타입 변환이란 기존 원시 값을 이용해 다른 타입의 새로운 원시 값을 생성하는 것이다.   

예제를 보게 되면,   
자바스크립트 엔진은 표현식 x + ''을 평가하기 위해 x 변수의 숫자 값을 바탕으로 새로운 문자열 값 '10'을 생성하고 이것으로 표현식 '10' + ''를 평가한다.   
암묵적으로 생성된 문자열 '10'은 x 에 재할당하지 않는다!   

즉, 암묵적 타입 변환은 기존 변수 값을 재할당하여 변경하는 것이 아니다.   
자바스크립트 엔진은 표현식을 에러 없이 평가하기 위해 피연산자의 값을 암묵적 타입 변환해 새로운 타입의 값을 만들어 단 한번! 사용하고 버린다.   