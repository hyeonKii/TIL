compiler는 소스 코드를 어셈블리어로 변환해주는 역할을 한다.   

과정은 다음과 같다.   

구문 분석 -> 최적화 -> 코드 생성 -> 링킹   

String tokenizer + Lexer -> Syntax Analyzer -> Semantic Analysis -> code optimizer -> target code   

 

Tokenizer

구문을 토큰화한다.   

토큰은 어휘 분석의 단위를 말한다.   

쉽게 생각해 구문을 1글자씩 자른다고 생각하면 된다.   

 

Lexer   

Lexer는 Tokenizer로 분해된 토큰들의 의미를 분석하는 역할을 한다.   

Tokenizer를 통해 의미 있는 단위로 분해되고, Lexer 거쳐 의미를 분석하는 과정을 Lexical Analyze 라고 한다.   

 Parser   

Lexical Anyalze 된 데이터를 구조적으로 나타낸다.   

데이터가 올바른지 검증하는 역할도 수행하는데 이를 모두 통틀어 Syntax Analyze 라고 한다.   

Parser를 통해 도출된 결과는 AST(Abstract Syntax Tree)를 만든다.   

AST(Abstract Syntax Tree)   

분석된 구문을 트리 형태로 나타낸 자료구조   

분석된 소스를 컴퓨터가 이해할 수 있는 구조로 변환된 트리라고 생각하면 된다.   