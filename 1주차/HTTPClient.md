# TCP/IP 통신

## TCP와 UDP
### 전송 계층의 대표적인 프로토콜
- TCP : 연결 필요O. 전달 및 순서 보장O (전화와 비슷)
- UDP : 연결 필요X. 전달 및 순서 보장X (편지와 비슷)

## Socket
### Socket vs Socket API
- Socket : 프로세스 간 통신의 종착점. 서버에서의 end point, 클라이언트에서의 end point가 연결이 되는 것. 이 둘이 연결되어서 어떻게 통신을 하느냐를 프로그래밍할 때 Socket API를 쓰는 것.
- Socket API : Berkeley Socket이라고 많이 부른다.

## TCP 통신 순서
