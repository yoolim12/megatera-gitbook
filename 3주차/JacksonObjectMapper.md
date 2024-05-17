# Jackson Object Mapper

## Spring 의존성 관리?
- @RestController - @Controller - @Component
- @SpringBootApplication - @ComponentScan
- @Component : Spring에서 @Component 어노테이션이 있는 메소드들을 자동으로 인식하여 객체 생성해줌

## Jackson Object Mapper
- Jackson Object Mapper를 사용하여 DTO <-> JSON 서로 변환 가능
- DTO : 필드보다는 getter 메소드의 이름을 따름
- @JsonProperty : key 이름 강제 변경
- objectMapper.writeValueAsString(postDto)를 통해 DTO -> String 변환
- Jackson을 바로 쓸 수 있는 이유는 Spring Boot가 Jackson을 지원하기 때문. 
- 변환 또한 Spring Boot에서 지원하기 때문에 실제로는 objectMapper.writeValueAsString(postDto)로 String 변환 작업 필요없이 return postDto; 로만 해줘도 자동으로 DTO -> String 변환이 된다.