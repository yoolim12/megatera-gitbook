# DTO

## DTO(Data Transfer Object)
- 참고 : https://martinfowler.com/eaaCatalog/dataTransferObject.html
- 말 그대로 데이터를 전송하는 객체
- "between processes" : 프로세스 간(대표적으로 DB와 BE) 데이터를 주고받는 객체

## IPC(Inter-Process Communication)
- 프로세스 간 통신
- IPC에서 쓸 수 있는 기술
  - File : 동시 접속 시 문제 -> 원격에서 사용하기에는 부적합
  - Socket : 원격 사용 O
  - HTTP
  - REST(HTTP + 필딩 제약조건) : RPC가 아닌 CRUD로 정리해야함
  - Java의 경우 RPC

## 개념 정리

### What is RPC & RMI?

**참고**<br/>
RPC : https://ko.wikipedia.org/wiki/%EC%9B%90%EA%B2%A9_%ED%94%84%EB%A1%9C%EC%8B%9C%EC%A0%80_%ED%98%B8%EC%B6%9C<br/>
RMI : https://ko.wikipedia.org/wiki/%EC%9E%90%EB%B0%94_%EC%9B%90%EA%B2%A9_%ED%95%A8%EC%88%98_%ED%98%B8%EC%B6%9C

RPC와 REST의 차이점은 무엇인가요? : https://aws.amazon.com/ko/compare/the-difference-between-rpc-and-rest/

