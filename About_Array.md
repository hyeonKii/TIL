### 배열

자바스크립트에서 배열은 List 객체다

자바스크립트의 배열은 비균질적이다 

= 메모리상에서 균질적인 데이터가 적재되지 않는다.

→ 배열에는 정수만 들어가는 것이 아닌 문자열, 더 중요한 것은 함수가 들어갈 수 있다.

### 배열에서 of, in 의 실체적 의미

전자 of 후자 ⇒ 후자의 존재를 iterator로 만들어준다.

iterator로 만들게 되면 for문 안에서 사용하게 될 때

for 블록문 안에서만 존재하고 종료 시, 메모리에서 사라진다. = freshness 상태

freshness = 메모리 상에서 고정상태가 아닌 상태