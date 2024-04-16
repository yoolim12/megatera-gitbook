# HTTP Server

## Socket 통신 실습 by Java
1. Listen
   - Listener 생성 : ServerSocket 클래스
   - ServerSocket
     - 파라미터로 port, backlog를 받는다.
     - backlog : requested maximum length of the queue of incoming connections.(큐에 대기시킬 개수, 그 외 나머지는 연결 끊김. 0이면 상황에 맞게 큐에 알아서 넣어줌.)

2. Accept
   - 클라이언트의 접속을 기다리고, 접속하면 소켓을 만들어줌.
   - Socket socket = listener.accept();

3. Request 받기
   - request를 먼저 받아야함 -> read 먼저
   - Reader reader = new InputStreamReader(socket.getInputStream());
   - request 받은 내용을 넣어줄 CharBuffer 생성.
   - 꼭 charBuffer.flip()!!!

4. Response
   - 응답 메시지를 만들어서 전송한다.
   - HTTP/1.1 200 OK<br/>
     (빈 줄)<br/>
     body(클라이언트한테 전송할 내용)
   - Writer writer = new OutputStreamWriter(socket.getOutputStream());
   - flush() : 현재 버퍼에 저장되어 있는 내용을 클라이언트로 전송하고 버퍼를 비운다.

5. Close