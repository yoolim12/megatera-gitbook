# Rest API

## API
- "어떻게 소통할 것이다"에 대한 명세

## REST(REpresentational State Transfer)
- 로이 필딩
  - REST architectural style과 다른 것들의 차별점은 REST는 컴포넌트 간(client, server)에 uniform interface를 쓴다는 것
  - 심플, 가시적
  - Decoupled(구현이 분리됨) -> interface를 통해 하기 때문
    -> 독립적으로 발전 가능
  - 단점 : standard form을 쓰기 때문에 다소 비효율적일 때도 있음.

## 필딩 제약조건
- uniform interface를 만족시키기 위한 제약조건 4개
  1. Identification of Resources -> URI 등으로 