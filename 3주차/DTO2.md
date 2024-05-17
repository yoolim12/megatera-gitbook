# DTO

## DTO(Data Transfer Object)
- https://martinfowler.com/eaaCatalog/dataTransferObject.html
- 원격(네트워크)로 프로세스 간 통신

## IPC(Inter-Process Communication)
- 서로 다른 프로세스 간의 통신
- IPC에서 쓸 수 있는 기술
  - File : 원격 환경 활용 X
  - Socket : 원격 환경 활용 O
    - HTTP
    - REST
      - Resource에 대한 CRUD
      - REST의 핵심 : resource, 표현
  - RPC(https://ko.wikipedia.org/wiki/%EC%9B%90%EA%B2%A9_%ED%94%84%EB%A1%9C%EC%8B%9C%EC%A0%80_%ED%98%B8%EC%B6%9C), RMI(https://ko.wikipedia.org/wiki/%EC%9E%90%EB%B0%94_%EC%9B%90%EA%B2%A9_%ED%95%A8%EC%88%98_%ED%98%B8%EC%B6%9C)

## DTO
- setter, getter로 이뤄짐
- = Java Bean = Bean (!= Spring Bean)(!= POJO)
- 무기력한 데이터 덩어리(Java에서는 클래스 말고 이를 구현할만한 구조체가 없음)

## Tier 간 통신
- F/E와 B/E 사이
  - DTO 그대로 전송 불가, 직렬화를 해야 전송 가능
  - 어떤 직렬화 기술? -> JSON, xml
- B/E와 DB 사이
  - Value Object(VO)가 아닌 Transfer Object