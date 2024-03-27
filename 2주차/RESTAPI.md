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

  3. Client-Stateless-Server(Section 3.4.3 - https://ics.uci.edu/~fielding/pubs/dissertation/net_arch_styles.htm#sec_3_4_3)
     - 서버에는 세션 상태를 저장 불가, 클라이언트에만 저장해야함.
     - 클라이언트에서 서버로 요청을 보낼 때, 요청을 이해할 수 있는 모든 정보를 포함해야하며, 서버에 저장된 정보를 사용할 수 없다.
     - 단점 : 서버에 있는 데이터를 클라이언트에 저장할 수 없기에, 반복적인 데이터가 발생 -> 네트워크 수행 능력이 떨어짐
  4. s