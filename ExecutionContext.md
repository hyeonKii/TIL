## Execution Context(실행 컨텍스트)


사전에 알아야할 지식

- 메모리에는 call stack과 memory heap이 존재
- Call stack은 메모리에 생성된다
- Cpu는 call stack을 만드는 역할
- Javascript Engine은 실행 컨텍스트를 담는 행위자 역할을 한다

1. Javascript Engine

    1) 엔진의 구성요소
        - Memory Heap
            메모리할당이 일어나는 곳
            참조타입(객체, 배열, 함수 등) 데이터가 저장된다.
            참조타입 데이터가 저장된 메모리힙의 주소값은 콜스택의 변수 식별자의 값으로 각각 저장된다.
            콜스택에 할당되는 변수 식별자 자체는 콜스택 상의 '실행 컨텍스트(Execution Context)의 렉시컬 환경(Lexical Environment) 라는 곳에 저장됨
            <br>
            <img src="https://velog.velcdn.com/images%2Fkirin%2Fpost%2Fdd74e18c-c465-44bd-935a-fa4e379d699d%2Fimage.png">
    
        - Call stack
            콜 스택(Call Stack)은 메모리에 존재하는 공간 중의 하나로, 코드를 읽어내려 가면서 수행할 작업들을 밑에서부터 하나씩 쌓고, 메모리 힙에서 작업 수행에 필요한 것들을 찾아서 작업을 수행하는 공간이다. 이런 구조를 LIFO(선입후출)구조라고 한다.cd 
    
