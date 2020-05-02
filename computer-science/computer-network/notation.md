---
description: 용어가 너무 어렵당... 그럼 정리해야지!
---

# Notation

### Computer Network\(컴퓨터 네트워크\)

* Communication Channel을 통해 연결되어있는 Communication Machine의 집합
* 이때, Communication Machine은 주로 Host, Router 등을 의미함

### Communication Channel\(통신 채널\)

* 정보를 포함하고 있는 바이트시퀀스를 이동시키는 매체
* ex\) Ethernet, dial-up Modem 등

### Host\(호스트\)

* Application이 실행되고 있는 User Computer, 혹은 Server Computer
* 컴퓨터 네트워크의 말단에 있는 장치 

### Router\(라우터\)

* 하나의 Communication Channel에서 다른 Channel로 정보를 중계, 전달하는 장치
* 세상에 모든 호스트들을 직접 연결하는 것은 **불가능! →** Router를 통해 그룹간 연결, 이로부터 인터넷을 구성/구현 

### Packet\(패킷\)

* 프로그램에 의해서 만들어진 정보를 포함하는 일련의 Byte들
* **User Data** : Application이 생성한 데이터
* **Control Data** : 프로토콜 계층을 통과하면서 추가되는 데이터 

### User Data

* Application 간에 전달되는 정보
* Network의 양 끝단에 있는 Host의 Application 간에만 의미를 가짐
* Packet이 경유하는 Router, Channel 등에선 단지 짐덩어리다. ~~\(오버워치의 화물같은 존재...?\)~~

### Control Data

* 목적지의 IP주소, 에러 대응용 코드 등 packet을 정확히 전달하기 위해 필요한 Data

### Payload\(화...물\)

* 각 프로토콜 계층에서 책임지고 전달해야 할 바이트시퀀스 

### Protocol\(통신규약\)

* 통신 프로그램간에 Packet을 교환하기 위한 약속
* Packet 구조의 정의, Encoding 방법 등 Packet을 교환하기 위한 모든 기술적 약속
* 통신상에 발생하는 문제들의 분야별로 프로토콜 그룹을 계층
* cf\) OSI의 7계층 - 네트워크에서 통신이 일어나는 과정을 나눈 

![](../../.gitbook/assets/image%20%285%29.png)

* 여기서 TCP/IP에 해당하는 레이어는 3-4레이어. \(중간지점.\) 

### Network Layer\(네트워크 계층\)

* Packet을 목적지에 정확히, 신속히 보내기 위한 경로설정과 관련한 기능을 수행하는 계층
* 이를 위해 **IP\(Internet Protocol\)**를 제공

### IP\(인터넷 프로토콜\)

* Host와 Host가 마치 연속적으로 연결된 것 처럼 하기 위해 두 호스트 간의 경로를 설정
* 집에서 회사까지 경로탐색하는 내비게이션과 비슷!
* IP는 Datagram을 기반으로 하는 Best-effort 프로토콜이다.

### Datagram

* IP프로토콜 간에 교환되는 Packet

![](../../.gitbook/assets/image%20%284%29.png)

* 같은 그룹의 Packet이 다른 경로로 전달될 수 있음. 따라서 이를 추후에 재조합할 수 있는 단서를 여기에 남겨둠

### Best-Effort Service

* 최선의 노력을 다하나, 물리적인 이유 등으로 인해 데이터손실이 날 수 있는 전송 서비

