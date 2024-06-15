# Layered Architecture

## Separation of Concerns(관심사의 분리)
- 기능(Business Logic - Spring MVC Controller)과 웹(UI Layer)의 분리
- 응집도 : 코드에 A라는 기능이 많이 뭉쳐져있느냐
- 결합도 : 코드에 A를 고쳤더니, B도 영향을 받는 경우는 결합도에 관한 것
- 대체로 응집도가 높으면, 결합도가 낮아짐(뭉쳐져있지 않고 분리되어 있을수록, 하나를 고쳤을 때 다른 하나가 영향을 받는 경우가 낮아짐)

## Identifier
- UUID
- ULID
  - 먼저 만든 순으로 ID 정렬됨
  - build.gradle에 의존성 추가
  - UlidCreator.getUlid().toString()
- TSID(Time-Sorted Unique Identifiers)
  - 시간 순 정렬 ID

## Extract Method
- https://refactoring.com/catalog/extractFunction.html

## Service
- 각 기능을 개별 메서드로 분리
- 관심사의 분리에 따라 코드도 분리
- 코드를 어떻게 배치하느냐 = 설계
- 설계를 고치는 것 = 리팩토링