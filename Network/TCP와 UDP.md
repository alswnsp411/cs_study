# TCP & UDP

## TCP 와 UDP 모두 프로토콜이다. 
![image](https://github.com/kksshh0612/cs_study/assets/81570533/3648f653-f062-4500-9c84-0df42e7cd1bb)<br>
TCP와 UDP는 전송계층에 해당하는 프로토콜로, 데이터 전송을 위해 포트 번호가 사용된다. 

🧹**프로토콜**이란? : 컴퓨터 내부 또는 컴퓨터 사이에 데이터를 교환하는 방식을 정의한 규칙이다. <br><br>

## TCP & UDP 의 등장 배경 
- IP의 한계 : IP(Internet Protocol)은 데이터를 패킷으로 감싸서 IP 주소를 통해 두 컴퓨터가 패킷을 주고 받는 프로토콜이다.<br>
![image](https://github.com/kksshh0612/cs_study/assets/81570533/4d691cfe-ea1e-4e59-99ff-1817ca1b52a9)
그런데, IP만을 이용한 통신에는 한계점이 있었다. 크게 두 가지가 있는데, <br>
1. **비신뢰성** : IP는 데이터 흐름에 관여하지 않고, 출발지 IP Address에서 목적지 IP Address가 패킷에 적혀있는 프로토콜이기 때문에
패킷이 **순서대로** 갔는지, 그리고 혹시 중간에 호스트가 강제로 종료되어 **유실**되진 않았는지 보장할 수 없다.<br>
2. **비연결성** : 패킷을 받을 상대 호스트가 연결 상태임을 확인하지 않는다. 따라서, 호스트가 강제 종료되어 있어도 패킷을 전송한다. <br><br>
▶️**이러한 한계를 극복하기 위하여 전송계층에서 TCP와 UDP 프로토콜을 추가 정의하였다.**

## TCP (Transmission Control Protocol)
- IP 패킷 전송을 제어하여 신뢰성을 보증함으로써 IP통신의 단점을 보완한 프로토콜이다.
- 보통 TCP/IP라 부르는데, IP 위에서 TCP가 동작하기 때문에 보통 그렇게 부르는 것이고, 둘은 별개의 프로토콜이다. <br>
IP에 따라 IP 주소를 찾고, TCP에 따라 어떤 포트에 어떤 순서로 정확하게 전달하는지 정해진다.

🧹**포트**란? : 어떤 프로세스가 해당 데이터를 처리하는지에 대한 정보이다. 프로세스는 각자 자신의 Port가 있고, 해당 Port를 통해 데이터를 주고받는다. 
ex) 아파치 톰캣 (스프링 내장 서버) default : 8080 <br><br>

![image](https://github.com/kksshh0612/cs_study/assets/81570533/6430e5bf-5b52-45db-a9c4-e6f09a2bdd27) <br>
TCP는 Application Layer에서 받은 데이터를 일정 단위로 분할해 각각 **TCP 헤더**를 붙여서 **TCP 세그먼트**를 생성한다.  
![image](https://github.com/kksshh0612/cs_study/assets/81570533/5c1742a0-bd4b-4ea7-871d-a5b7d982a360)

### TCP Segment 헤더 구조 
![image](https://github.com/kksshh0612/cs_study/assets/81570533/ab7969aa-7769-4232-bf15-3f43446453d2)




➕참고자료 
- <a href="https://inpa.tistory.com/entry/WEB-%F0%9F%8C%90-TCP-IP-%EC%A0%95%EB%A6%AC-%F0%9F%91%AB%F0%9F%8F%BD-TCP-IP-4%EA%B3%84%EC%B8%B5">Inpa - TCP/IP 4계층</a>
- <a href="https://inpa.tistory.com/entry/WEB-%F0%9F%8C%90-OSI-7%EA%B3%84%EC%B8%B5-%EC%A0%95%EB%A6%AC#tcp/ip_4%EA%B3%84%EC%B8%B5">Inpa - OSI 7계층</a>
- <a href="https://inpa.tistory.com/entry/NW-%F0%9F%8C%90-%EC%95%84%EC%A7%81%EB%8F%84-%EB%AA%A8%ED%98%B8%ED%95%9C-TCP-UDP-%EA%B0%9C%EB%85%90-%E2%9D%93-%EC%89%BD%EA%B2%8C-%EC%9D%B4%ED%95%B4%ED%95%98%EC%9E%90#%F0%9F%95%B9%EF%B8%8F_tcp%EC%9D%98_%EC%A0%84%EC%86%A1_%EC%A0%9C%EC%96%B4_%EA%B8%B0%EB%B2%95">Inpa - TCP, UDP</a>
- <a href="https://kotlinworld.com/94">TCP</a>
- <a href="https://nogan.tistory.com/20">TCP 세그먼트 구</a>
- <a href="https://kotlinworld.com/94">TCP</a>
