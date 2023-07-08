## 코드 실행 순서

1. 전역객체 생성(메모리의 data영역에 적재)
2. global 코드 평가(not 실행)

    #2 global 평가 단계에서 아래와 같이 생성

    실행 컨텍스트 생성

    렉시컬 환경 생성 - 환경레코드, 아우터, globalThisValue

    환경레코드에는 object envrecord(bind object를 내포), declarative envrecord(let, const 내포)가 존재

    *declarative envrecord는 전역 실행컨텍스트에만 존재

    *bind object는 전역 객체(var, function 내포)를 가리키고 있다.

    *블록문은 실행컨텍스트를 타지 않는다(블록을 탈수도 타지 않을 수도 있기에)

3. global 코드 실행
4. 함수 코드 평가(이 때 arguments 객체를 만들어 놓는다)
5. 함수 코드 실행