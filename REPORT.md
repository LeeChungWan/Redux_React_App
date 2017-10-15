Redux란 무엇인가?

- 핵심
	Redux는 어플리케이션의 클라이언트쪽 state를 관리하기 위한 거대한 event loop이다.
	Action = Event, Reduxer = Event에 대한 반응.

- Redux 등장배경
	º facebook에서 react와 함께 소개한 Flux 아키텍쳐를 구현하기 위한 라이브러리
	º 컴포넌트 간 state 데이터를 효율적으로 관리하기 위해 등장
	º Flux 와 MVC 패턴의 차이
 		▶ MVC 패턴은 앱의 규모가 커지면 그에 따라 model과View가 늘어나기에 프로젝트가 복잡해진다.
		▶ Model과 View가 1:1 관계가 아니므로 데이터 관리도 어렵다는 단점이 있다.
	º Redux는 facebook에서 만든 라이브러리는 아니다.
	º react를 공부하고 간단한 프로젝트를 하다보면 state 데이터 관리에 신경쓰게 된다.
	º 기존 앱에 기능이 추가되고, 그에 따라 컴포넌트가 추가 되다보면 state 데어터 관리가 힘들어진다.

- Redux의 특징
	º 단 하나의 store만 존재한다.(flux는 여러개의 store 사용)
	º store에 있는 state는 Read-only 속성이며, state를 핸들링 하러면 반드시 action을 통해야 한다.
	º reducer는 pure function 해야 한다. (action 객체를 처리하는 함수를 reducer라 부른다.)
	º pure function이라 함은, 함수 내부 로직에 네트워크 통신이나 데이터베이스 접근등 행위가 이루어지지 않음을 뜻한다.
	º reducer는 action에서 받은 정보를 어떻게 업데이트 할지만 정의.
