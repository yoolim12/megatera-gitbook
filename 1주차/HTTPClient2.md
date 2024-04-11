# HTTP Client

## TCP/IP 통신

## TCP와 UDP
- TCP
  - 연결 필수
  - 전달, 순서 보장
  - 전화와 비슷
- UDP
  - 연결 필수X
  - 전달, 순서 보장X
  - 편지와 비슷

## Socket
- Socket vs Socket API
- Socket API : https://en.wikipedia.org/wiki/Berkeley_sockets
- Socket : https://ko.wikipedia.org/wiki/%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC_%EC%86%8C%EC%BC%93

## TCP 통신 순서
1. 서버는 접속 요청을 받기 위한 소켓을 연다.(Listen)
2. 클라이언트는 소켓을 만들어서, 서버에 접속 요청(Connect)
3. 요청을 받은 서버는, 통신할 소켓을 따로 또 만듦(Accept)
4. 해당 소켓을 통해 서로 데이터 주고 받음(Send & Receive)
5. 서버나 클라이언트 둘 중 하나가 통신 마친 후 소켓 닫음(Close)

## Socket 통신 실습 by Java
1. Connect
    - host, port 필요
    - host : IP 주소 또는 도메인 주소
    - Socket socket = new Socket(host, port);
2. Request
    - 요청 메시지를 만들어 TCP로 전송
    - GET http://example.com/ HTTP/1.1<br/>(빈 줄)
    - 또는 GET / HTTP/1.1<br/>Host: example.com<br/>(빈 줄)
    - 
3. dddd