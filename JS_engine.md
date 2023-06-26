### 자바스크립트 엔진

자바스크립트 엔진 내부에서 코드를 분석 하는 과정   

parser가 lexical analysis를 거쳐 AST가 생성된다.   
AST 구조가 Interpreter와 만나 byte code로 변환된다.   
compile 이 필요할 경우, profiler가 확인해서 compiler로 optimized code로 변환한다.   
optimized 된 코드들은 target code로 최종적으로 변환된다.   

자바스크립트 내부에 존재하는 call stack 과 heap은 논리적 구조다.   
실제 메모리에는 자바스크립트 엔진을 통해 파싱된 코드들이 코드와 데이터, stack, heap 영역에 적재된다. 