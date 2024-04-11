# REST API

## F/E와 B/E
- FrontEnd 와 BackEnd 사이를 연결하는데에 REST API, SOAP API, GraphQL API 등을 사용

## API(Application Programming Interface)
- 컴퓨터나 컴퓨터 프로그램 사이의 연결

## Roy Fielding의 REST API 논문
- 참고 : 
  - https://ics.uci.edu/~fielding/pubs/dissertation/rest_arch_style.htm
  - https://m.blog.naver.com/aservmz/222234406469

  - REST : 소프트웨어 아키텍처 + 제약조건

- 제약조건
  1. NULL 스타일로 시작 : REST를 시작하기 위한 시작 조건. 설계자는 아무 것도 없는 상태에서 설계를 시작해서, 제약조건을 점점 추가해나가는 것

  2. Client-Server
      - 관심사의 분리(사용자에 대한 관심사 - 데이터에 대한 관심사)
      - 클라이언트, 서버 각각이 독립적으로 발전할 수 있도록 함

  3. Client-"Stateless"-Server(Section 3.4.3 - https://ics.uci.edu/~fielding/pubs/dissertation/net_arch_styles.htm#sec_3_4_3)
     - 서버에는 세션 상태를 저장 불가, 클라이언트에만 저장해야함.
     - 클라이언트에서 서버로 요청을 보낼 때, 요청을 이해할 수 있는 모든 정보를 포함해야하며, 서버에 저장된 정보를 사용할 수 없다.
     - 단점 : 서버에 있는 데이터를 클라이언트에 저장할 수 없기에, 반복적인 데이터가 발생 -> 네트워크 수행 능력이 떨어짐

  4. Client-"Cache"-Stateless-Server(Section 3.4.4 - https://ics.uci.edu/~fielding/pubs/dissertation/net_arch_styles.htm#sec_3_4_4)
      - 캐시는 요청에 대한 응답이 "cacheable" 이라는 가정 하에, 이후에 들어오는 요청에 대한 응답이 이전에 왔던 요청에 대한 응답과 비슷할 경우, 응답을 재사용할 수 있도록 해준다.
      - 쉽게 말해, 클라이언트와 서버 사이의 중개자 역할을 한다.
      - 단점 : 캐시에 있는 이전 데이터(이전 응답)가 현재 서버에 보냈다면 나올 응답과 다른 경우가 생길 수 있음 -> 신뢰도 하락

  5. Uniform Interface
      - 컴포넌트 간(Client와 server)에 uniform interface 사용
      - 웹에도 일반적인 소프트웨어공학에서의 원칙 적용
      - decoupled(분리된) 구현 ("interface" 를 사용하기 때문에) -> 독립적으로 발전 가능
      - 단점 : 정해진 규칙들을 따라야 하기에 효율성 down
      - 대규모 하이퍼미디어 데이터를 주고 받는, 웹에서의 일반적인 경우에는 효과적 BUT 예외적인 경우에는 효과적이지 못할 수 있다.
      - uniform interface가 되기 위해 REST에 4가지 interface 제약 조건들을 걸었다 -> 이것이 필딩 제약 조건
      - 필딩 제약 조건(REST라고 할 때는 대개는 필딩 제약 조건을 따르느냐 안 따르느냐를 먼저 본다)
        - 4가지 인테페이스 제약조건
          1. Identification of Resources -> URI 등으로 리소스를 식별 가능
          2. Manipulation of Resources through Representations -> 표현으로 리소스를 조작한다.
          3. Self-Descriptive Messages - 자기서술적인 메시지를 사용해야 한다.
          4. HATEOAS(Hypermedia As The Engine Of Application State)

        - 아키텍처 요소에서 리소스와 표현을 구분
          - Resource
            - 추상
            - 모든 시간에 통용되는 엔티티 집합
            - <객체지향의 사실과 오해> -> "앨리스" 라는 리소스는 키가 커지던, 작아지던 항상 "앨리스" 다.
            - 즉 값이 변하더라도 그 자체는 변하지 않는다? 라는 뜻인 것 같다.
          - Representation
            - 데이터

  6. Layered System - 여러개의 Layer로 구성된다.
  7. Code-On-Demand