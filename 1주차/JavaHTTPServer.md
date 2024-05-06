# Java HTTP Server

## Java HTTP Server
- 내부적으로 NIO(Non-blocking I/O)를 사용하는 고수준 HTTP 서버 API
- https://en.wikipedia.org/wiki/Non-blocking_I/O_(Java)

## HTTP Server 실습 by Java Server

1. ## 서버 객체 준비
   - HttpServer httpServer = HttpServer.create(address, backlog);
   - address는 InetSocketAddress 클래스를 통해 얻는다.
2. ## URL(정확히는 Path)에 핸들러 지정
   - ### createContext 함수
     - param : String path, HttpHandler handler
     - HttpHandler 인터페이스
       - handle 함수 하나만 존재
       <br> -> 인터페이스에 메소드가 하나만 있는 경우 람다로 표현 가능
   - httpServer.createContext("/", (exchange) -> {
        <br>// TODO
    <br>});

   - ### Request
        - HTTP Method
        - HTTP Path
        - Headers
        - Body

   - ### Response
        - 데이터를 byte 배열로 준비
        - HTTP Status Code와 Content-Length 지정
        - 데이터 전송

3. ## Listen
   - httpServer.start();