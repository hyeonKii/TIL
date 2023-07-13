객체의 프로퍼티의 키와 값은는 실행 컨텍스트 상에서 어디에 담길까?

→ 전역 객체에 Variable Table이 존재 / 함수 EnvRecord에도 VariableTable 존재. 따라서 키는 VariableTable에 적재되고 값은 EnvRecord에 존재