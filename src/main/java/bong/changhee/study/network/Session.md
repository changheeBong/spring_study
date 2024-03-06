## Session
***
### 등장배경
***
웹 애플리케이션은 클라이언트의 요청에 대해 동적으로 페이지를 생성하고, 클라이언트의 상태를 유지해야 하는 경우가 많다. <br>
예를 들어, 로그인 상태를 유지하면서 http로 개인 정보를 주고 받다보면 쿠키가 유출, 조작될수 있는 큰 문제를 야기시킨다.

session은 인증 정보를 쿠키에 저장하지 않고 식별자를 사용하면서 상태 정보를 저장하기 위해 등장하였다.

### Session이란?
***
웹 애플리케이션에서 클라이언트와 서버 간의 상태 정보를 유지하고 관리하기 위해 중요한 요소이다. <br>
HTTP 프로토콜은 기본적으로 상태를 유지하지 않는 stateless 프로토콜이기 때문에, 세션은 클라이언트와 서버 간의 상태 정보를 추적하고 유지하기 위해 사용된다.

### Session 활용 예시
***
사용자가 웹 애플리케이션에 접속할 때 서버는 해당 사용자에 대한 고유현 세션을 생성한다. <br>
이 세션에 관련된 데이터를 저장하기에 다음과 같이 사용될 수 있다.
* 로그인 정보 유지 : 사용자의 로그인 상태를 추적하고, 인증된 사용자인지 확인
* 상태 정보 저장 : 사용자의 장바구니, 선호 설정 등과 
* 데이터 공유 : 서버의 여러 페이지나 요청 간에 데이터를 공유

### 생명주기
***
세션은 일정 시간 동안 유지되며, 클라이언트의 비활동 시간이 일정 시간 이상 지속될 경우 만료된다. 세션의 생명주기는 다음과 같은 단계로 구성된다.
* 세션 생성 : 클라이언트 접속 시 서버는 고유한 세션 ID를 생성하고, 클라이언트에게 전달
* 세션 유지 : 클라이언트가 세션 ID를 서버에 전달하면, 서버는 해당 세션에 대한 상태 정보를 유지
* 세션 만료 : 일정 시간 동안 클라이언트의 요청이 없을 경우 세션은 만료된다.
  * 만료된 세션은 클라이언트의 요청 시 재생성

### 단점
* 서버 메모리 부하
세션은 서버 메모리에 저장되기 때문에 많은 사용자가 동시에 접속하는 경우 서버의 메모리 부하가 증가할 수 있다.
* 확장성 문제 :
세션은 단일 서버에 의존하기 때문에, 클러스터링이나 부하 분산을 위해 추가 구현이 필요하다.
* 데이터 손실 위험 :
서버 장애 또는 재시작 시 세션 데이터의 손실이 발생할 수 있다.
* 보안 문제
세션 ID를 탈취하거나 세션 하이재킹 (Session Hijacking)과 같은 공격으로부터 안전하지 않을 수 있다.





































