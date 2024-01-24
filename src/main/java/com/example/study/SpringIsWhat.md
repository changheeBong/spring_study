
스프링이란 무엇인가
스프링이란?
 자바 애플리케이션 개발을 도와주는 프레임워크 이다.
 애플리케이션의 틀, 공통 프로그래밍 모델, 기술 API 등을 제공한다.
 스프링 컨테이너
  스프링 컨테이너 혹은 애플리케이션 컨텍스트로 불리는 스프링 런타임 엔진이다.
  설정 정보를 참고하여 오브젝트를 만들고 관리한다.
  독립적으로 사용 가능하나, 웹 모듈에서 동작하는 서비스, 서블릿으로 등록해 사용한다.

 공통 프로그래밍 모델 - IoC/DI,서비스 추상화, AOP
  공통 프로그래밍 모델
    스프링은 공통 프로그래밍 모델을 통해 애플리케이션 코드가 어떻게 작성돼야 하는지에 대한 기준을 제공한다.

 IoC/DI
  IoC/DI는 스프링이 제공하는 모든기술,API,컨테이너의 기반이 되는 기술이다.
  IoC/DI의 설명 링크

 서비스 추상화
  환경,서버,특정 기술에 종속되지 안흔 이식성 뛰어난 유연한 애플리케이션을 작성하는 토대이다.
  주로, 유연한 추상 계층을 둠으로써 구현된다.
  ex)자바의 다형성을 기반으로 구현할 수 있다.

  AOP(Aspect Oriented Programming)
   애플리케이션 코드에 산재해서 나타나는 부가적인 기능을 독립적으로 모듈화 하는 프로그래밍 모델이다.
   ex) 모든 메소드에 적용되는 로깅, 소요시간 측정 등에 적용할 수 있다.

  기술 API
  웹 프레젠테이션, 비즈니스 서비스, 기반 서비스, 도메인, 데이터 엑세스 계층 등에서 필요한 주요 기술 및 전략 클래스 등을 스프링에서 일관된 방식으로 사용할수 있도록 지원한다.
  스프링의 모든 기술은 표준 자바 EE에 기반을 두고 있다.

  종합 정리
  IoC/DI : 스프링 컨테이너 위에 직접 작성한 클래스를 오브젝트로 올려 활용할 수 있따.
  공통 프로그래밍 모델 : 스프링의 공통 프로그래밍 모델을 따라 스프링이 지향하는 방향으로 코드를 작성할 수 있다.
  기술 API 및 서비스 : 엔터프라이즈 기술을 사용할 때 활용한다.

  스프링의 성공 요인
  자바 엔터프라이즈 개발의 핵심 가치에 충실하여 베스트 프랙티스 적용에 용이
  이상적인 개발철학,프로그래밍 모델은 이해에 도움이 되고 좋은 개발 습관을 만듦
  가장 중요한 두가지 가치인 단순함과 유연성을 강조했음

  단순함
   기존 EJB라는 표준 기술의 복잡함을 타파함. 스프링은 가장 단순한 객체지향적인 개발 모델인 POJO 프로그래밍을 지향함
  유연성
   항상 "프레임워크 기반의 접근 방법을 사용하는 것"이 핵심 철학임
많은 서드파티 프레임워크의 지원을 받지만 코드베이스가 흔들리거나 새로 만드는 일이 없었음

   스프링 학습 방법
   스프링의 핵심 가치와 원리에 대한 이해
   핵심 가치를 이해하고, 핵심 가치를 이룰 수 있도록 도와주는 세 가지 핵심 기술을 이해하라.
   스프링이 강조하는 중요한 프로그래밍 모델을 이해하고, 스프링을 일관된 방식으로 이해할 수 있는 눈을 갖춰라

   스프링 기술에 대한 지식과 선택 기준 정립
    다양한 선택의 문제를 각 기술 영역별로 효과적으로 다루는 방법을 배워야 한다.
스프링은 애플리케이션의 모든 레이어를 폭 넓게 다루며 영역별로 다양한 접근 방법을 제공한다.
많은 방법 중 어떤 것을 선택할 것인지, 어떤 것을 연동할 것인지, 어떤 스타일을 사용할 것인지
상황에 따른 최선의 방법을 선택할 수 있어야 한다.

스프링의 적용과 확장.
스프링이 제공하는 기능을 확장, 추상화할 줄 알아야 한다.
스프링을 기반으로 새로운 프레임워크를 만들 수 있으면 바람직하다.
때론 스프링의 자유도를 줄이고, 현장 상황에 맞는 접근방법을 정립해줄 수 있어야 한다.
스프링이 지원하지 않는 기술을 스프링에 맞게 통합할 수도 있어야 한다.

스프링의 핵심
기본으로 돌아가 객체지향 프로그래밍이 제공하는 폭 넓은 혜택을 누리자
객체지향 기술과 설계, 구현에 관한 실용적인 전략과 검증된 베스트 프랙티스를 평범한 개발자도 자연스럽고 손쉽게 이용할 수 있게 만들자
User DAO
DAO는 DB를 사용해 데이터를 조회하거나 조작하는 기능을 전담하도록 만든 오브젝트를 말한다.
User 클래스 작성
User 클래스는 자바빈 규약을 따르는 오브젝트이다.
 자바빈(JavaBean)은 원래는 비주얼 툴에서 조작 가능한 컴포넌트를 말했으나, 현재는 디폴트 생성자를 갖추고 , 프로퍼티를 가진 오브젝트를 말한다.
 디폴트 생성자를 갖추는 이유는 리플렉션을 이용해 오브젝트를 생성할 수 있어야 하기 때문이다.

관심사의 분리
변화에 어떻게 대응할 것인가?
핵심은 변화에 어떻게 대응할 것인가이다. 객체지향설계와 프로그래밍은 절차적 프로그래밍 패러다임에 비해 조금 더 많은 초기 비용을 소모한다..
많은 번거로운 작업들이 요구된다. 그러나 , 처음에만 이러한 수고를 하여 제대로 객체지향 설계를 해두면, 객체지향 기술의 특성으로 변화에 효과적으로 대응할 수 있다.

객체지향 기술은 가상의 추상세계 자체를 효과적으로 구성할 수 있고, 이를 자유롭고 편리하게 변경, 발전 확장시킬 수 있다.
변경이 일어날 때, 필요한 작업을 최소화하고 그 변경이 다른 곳에 문제를 일으키지 않게 하려면 어떻게 해야할까? 분리와 확장을 고려한 설계를 해야한다.

변화에서의 관심사
보통 변화에서의 관심사는 단 한 곳에서 일어나느 반면, 잘 설계되지 못한 프로그램을 변화시키려면 수백 개의 클래스를 수정해야 할 수도 있다.
 DB의 계쩡과 암호라는 단 하나의 관심사만 변경하려 해도, 초모든 dao 코드를 뒤집어 엎어야 할 수 있다.

단 한 곳의 관심사를 수정할 때, 단 한 곳의 코드만 수정하면 되도록 바꾸는 것이 우리의 저냙이다.

관심사 분리의 핵심
 변화가 일반적으로 한 번에 한가지 관심에 집중돼서 일어난다는 것을 알았으니, 관심이 같은 것 끼리는 모으고, 관심이 다른 것은 따로 떨어져 있게 하는 것으로써 변화에 대비할 수 있다.

관심사의 분리는 관심이 같은 것끼리는 하나의 객체 안으로 또는 친한 객체로 모이게 하고, 관심이 다른 것은 가능한 한 따로 떨어져서 서로 영향을 주지 않도록 분리하는 것이다.
  관심사 분리는 처음부터 완벽하게 설계된 채로 할 수는 없다. 처음에는 몽뚱그려 쉽게 코딩하더라도 설계를 생각하며 지속적 리팩토링을 거치는 과정이 중요하다고 생각한다.

UserDao의 관심사 뽑아보기
 총 3가지의 관심사가 나온다.
 DB와 연결하기 위한 커넥션을 가져오는 것
 DB에 보낼 SQL 문장을 담을 Statement를 만들고 실행하는 것
 공유 리소스를 시스템에 돌려주는 것

중복 코드를 메소드로 추출하기
현재 마주한 가장 큰 문제는 위의 .add() 메소드의 관심사 코드가 .get() 에도 중복되어 있다는 것이다.
앞으로 DAO를 만들 때 마다 이렇게 중복된 관심사 코드가 발생하면, 변경이 일어날 때 엄청난 고통을 일으킬 수 있다. 중복된 코드를 메소드로 추출하자.

변경사항에 대한 검증하기: 리팩토링과 테스트
    위와 같이 코드에 변화가 일어난 후에는 반드시 제대로 작동하는지 다시 테스트 해보아야 한다. 초난감 DAO에서 작성한 main 메소드는 현재까지
    그럭저럭 테스트 코드의 역할을 해줄 수 있다. 물론 현재는 등록한 회원을 DB에서 수동으로 지우지 않으면 기본키가 겹쳐서 에러가 뜨겠지만 말이다.

리펙토링의 의미
이번 작업에서 UserDao의 기능은 단 하나도 변하지 않았다. 다만, 중복된 코드가 사라져 이전보다 조금 더 깔끔해지고, 미래의 변화에 좀 더 손쉽게 대응할 수 있는 코드가 됐다.
이러한 작업을 리팩토링이라고 한다.

메소드로 중복된 코드를 뽑아내서 정리하는 것을 리팩토링에서는 메소드 추출 기법이라고 한다. 리팩토링은 객체지향 개발자라면 반드시 익혀야 하는 기법이다.

이 과정에서 기능을 추가하기보다는 코드 구조와 구현 방법을 바꿈으로써 더 나은 DAO를 만드는데 주력했다. 앞으로 이러한 작업을 리팩토링이라고 부르겠다.

리팩토링의 정의
기존 코드를 외부의 동작 방식에는 변화없이 내부 구조를 변경해서 재구성하는 작업 또는 기술을 말한다.
코드 내부의 설계가 개선되고 코드를 이해하기가 편해진다. 이로 인해 변화에 효율적으로 대응할 수 있다.
생산성은 올라가고 코드의 품질은 높아지며 유지보수하기 용이해지고 견고하면서도 유연한 제품을 개발할 수 있다.

리팩토링이 필요한 코드의 특징을 나쁜 냄새 라고 부르기도 한다. 중복 코드는 매우 흔하게 발견되는 나쁜 냄새이다. 적절한 리팩토링 방법을 적용해 나쁜냄새를 제거해주어야 한다.

리팩토링은 개발자가 직관적으로 수행할 수도 있지만 본격적으로 적용하려면 학습과 훈련이 필요하다. 나쁜 냄새에는 어떤 종류가 있고 그에 따른 적절한 리팩토링 방법은 무엇인지 알아보고
충분한 연습을 해두면 도움이 된다.

템플릿 메소드 패턴
상속을 통해 슈퍼클래스의 기능을 확장할 때 사용하는 가장 대표적인 방법이다.
슈퍼 클래스에 기본적인 로직의 흐름을 만들고, 기능의 일부를 추상 메소드나 오버라이딩이 가능한 protected 메소드 등으로 만든 뒤 서브 클래스에서 이런 메소드를 필요에 맞게 구현해 사용하는 방법을
디자인 패턴에서 템플릿 메소드 패턴이라고 한다.

슈퍼 클래스에서 디폴트 기능을 정의해두거나 비워뒀다가 서브 클래스에서 선택적으로 오버라이드할 수 있도록 만들어둔 메소드를 훅(hook) 메소드라고 한다.
서브 클래스에서는 훅 메소드를 오버라이드하여 기능의 일부를 확장한다.

팩토리 메소드 패턴
템플릿 메소드 패턴과 마찬가지로 상속을 통해 기능을 확장하게 하는 패턴이다. 서브 클래스에서 구체적인 오브젝트 생성 방법을 결정하게 하는 것을 팩토리 메소드 패턴이라고 부른다.
주로 인터페이스 타입으로 오브젝트를 리턴하므로 서브클래스에서 정확히 어떤 클래스의 오브젝트를 만들어 리턴할지

서브 클래스에서 오브젝트 생성 방법과 클래스를 결정할 수 있또록 미리 정의해둔 메소드를 팩토리 메소드라 하며 이 방식을 통해 오브젝트 생성 방법을 슈퍼 클래스에서 독립시키는 방법을
팩토리 메소드 패턴이라고 한다.

자바는 종종 오브젝트를 생성하는 기능을 가진 메소드를 팩토리 메소드라고 부르기도 한다. 이 때 말하는 팩토리 메소드와 팩토리 메소드는 의미가 다르므로 혼동하지 않도록 주의해야 한다.

디자인 패턴
디자인 패턴을 잘 아는 개발자라면 "UserDao에 팩토리 메소드 패턴을 적용해서 getConnection()을 분리합시다."라는 한마디로 앞에 배웠던 내용을 한 문장으로 정리할 수 있따.

디자인 패턴은 소프트웨어 설계시 특정 상황에서 자주 만나는 문제를 해결하기 위해 사용할 수 있는 재사용 가능한 솔루션을 말한다. 모든 패턴에는 간결한 이름이 있어서 간단히 패턴 이름으로
설계 의도와 해결책을 함께 설명할 수 있다는 장점이 있다.

디자인 패턴은 주로 객체지향 설계에 관한 것이며, 객체지향적 설계 원칙을 이용해 문제를 해결한다. 패턴의 설계 구조는 생각보다 대부분 비슷한데, 그 이유는 문제를 해결하기 위한 방법을 선택할 때, 클래스 상속과
오브젝트 합성이라는 두가지 길에서 크게 벗어나지 않기 때문이다.
패턴에서 가장 중요한 것은 각 패턴의 핵심이 담긴 목적 또는 의도이다. 패턴을 적용할 상황, 해결해야 할 문제, 솔루션의 구조와 각 요소의 역할과 함께 핵심 의도가 무엇인지 잘 기억해두어야 한다.

상속의 단점
상속을 사용하는 것은 장점은 있을 것 같지만, 사실 단점도 크다.

 - 자바는 다중 상속을 지원하지 않으므로, 단 한번 상속을 이용하면 다른 오브젝트를 또 상속할 수는 없다.
 - 상속을 통한 상하위 클래스 관계는 생각보다 밀접하다.
  슈퍼클래스의 변경이 있을 때, 서브클래스를 함께 수정해야 하거나 다시 개발해야 할 수 있다.
  위와 같은 변화를 주지 않기 위해 슈퍼클래스의 변화가 일어나지 않도록 제약을 가해야 할지도 모른다.
