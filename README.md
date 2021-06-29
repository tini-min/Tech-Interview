# Tech Interview

**개인적으로 기술 면접을 대비하면서 작성한 Repository 입니다.**
> :star: 내용에 오류가 있거나 추가할 내용이 있다면 Pull Request를 통해서 알려주시면 감사하겠습니다.
> <br>:star: Star나 RP를 통한 많은 관심 부탁드립니다.

**:book: Contents**
1. [Operating System](https://github.com/tini-min/Tech-Interview/tree/master/OS/)

    <details>
    <summary><strong>목차</strong></summary>
    <div markdown = "1">

    - [운영체제의 역활은 무엇입니까?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#운영체제의-역활은-무엇입니까)
        * [커널 모드와 사용자 모드는 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#커널-모드와-사용자-모드는-무엇인가요)
        * [시스템 콜은 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#시스템-콜은-무엇인가요)
    - [프로세스와 스레드는 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#프로세스와-스레드는-무엇인가요)
        * [PCB는 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#pcb는-무엇인가요)
        * [프로세스의 상태 전이를 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/OS/#프로세스의-상태-전이를-설명해-주세요)
        * [커널 레벨 스레드와 유저 레벨 스레드가 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#커널-레벨-스레드와-유저-레벨-스레드가-무엇인가요)
        * [IPC는 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#ipc는-무엇인가요)
            + [IPC 종류와 특징에 대해 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/OS/#ipc-종류와-특징에-대해-설명해-주세요)
    - [멀티 스레드와 멀티 프로세스가 무엇이고, 각각의 장단점은 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#멀티-스레드와-멀티-프로세스가-무엇이고-각각의-장단점은-무엇인가요)
        * [멀티 스레딩 시 스레드마다 스택과 PC를 독립적으로 할당하는 이유는 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#멀티-스레딩-시-스레드마다-스택과-pc를-독립적으로-할당하는-이유는-무엇인가요)
        * [Thread-Safe란?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#thread-safe란)
            + [Reentrant가 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#reentrant가-무엇인가요)
        * [Context Switching이 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#context-switching이-무엇인가요)
    - [경쟁 상태란 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#경쟁-상태란-무엇인가요)
        * [Critical Section(임계영역)과 Critical Section Problem(임계영역 문제)가 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#critical-section임계영역과-critical-section-problem임계영역-문제가-무엇인가요)
        * [동기화란 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#동기화란-무엇인가요)
            + [동기화와 관련된 고전적인 문제들을 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/OS/#동기화와-관련된-고전적인-문제들을-설명해-주세요)
            + [동기화를 제공하는 방식에 대해 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/OS/#동기화를-제공하는-방식에-대해-설명해-주세요)
            + [스핀락과 뮤텍스의 차이는 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#스핀락과-뮤텍스의-차이는-무엇인가요)
            + [뮤텍스와 세마포어의 차이는 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#뮤텍스와-세마포어의-차이는-무엇인가요)
        * [교착상태에 대해 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/OS/#교착상태에-대해-설명해-주세요)
    - [인터럽트가 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#인터럽트가-무엇인가요)
        * [인터럽트 기능이 없으면 어떤 일이 발생하나요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#인터럽트-기능이-없으면-어떤-일이-발생하나요)
    - [스케줄러란 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#스케줄러란-무엇인가요)
        * [각 스케줄러의 기능은 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#각-스케줄러의-기능은-무엇인가요)
            + [Swapping이 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#swapping이-무엇인가요)
        * [CPU 스케줄러의 목표는 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#cpu-스케줄러의-목표는-무엇인가요)
        * [CPU 스케줄러(단기 스케줄러)의 종류에 대해 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/OS/#cpu-스케줄러단기-스케줄러의-종류에-대해-설명해-주세요)
    - [동기와 비동기, Blocking과 Non-Blocking은 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#동기와-비동기-blocking과-non-blocking은-무엇인가요)
    - [메모리 관리 기법에 대해서 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/OS/#메모리-관리-기법에-대해서-설명해-주세요)
        * [연속 메모리 관리와 불연속 메모리 관리에 대해서 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/OS/#연속-메모리-관리와-불연속-메모리-관리에-대해서-설명해-주세요)
    - [가상 메모리는 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#가상-메모리는-무엇인가요)
        * [가상 주소 공간이 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#가상-주소-공간이-무엇인가요)
        * [요구 페이징이란 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#요구-페이징이란-무엇인가요)
        * [페이지 부재와 페이지 교체에 대해 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/OS/#페이지-부재와-페이지-교체에-대해-설명해-주세요)
        * [페이지 교체 알고리즘은 어떤 것들이 있습니까?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#페이지-교체-알고리즘은-어떤-것들이-있습니까)
            + [LRU 알고리즘과 NUR 알고리즘의 차이점은 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#lru-알고리즘과-nur-알고리즘의-차이점은-무엇인가요)
            + [Page Reference String은 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#page-reference-string은-무엇인가요)
        * [MMU가 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/OS/#mmu가-무엇인가요)

    </div>
    </details>

1. [Network](https://github.com/tini-min/Tech-Interview/tree/master/Network/)

    <details>
    <summary><strong>목차</strong></summary>
    <div markdown = "1">

    - [OSI 7계층이 무엇이고 이를 나누는 이유가 무엇입니까?](https://github.com/tini-min/Tech-Interview/tree/master/Network/#osi-7계층이-무엇이고-이를-나누는-이유가-무엇입니까)
        * [OSI 7계층의 각 계층을 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/Network/#osi-7계층의-각-계층을-설명해-주세요)
        * [전이중 통신과 반이중 통신이 무엇입니까?](https://github.com/tini-min/Tech-Interview/tree/master/Network/#전이중-통신과-반이중-통신이-무엇입니까)
        * [ARP가 무엇입니까?](https://github.com/tini-min/Tech-Interview/tree/master/Network/#arp가-무엇입니까)
    - [TCP와 UDP의 장단점을 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/Network/#tcp와-udp의-장단점을-설명해-주세요)
        * [가상회선 패킷 교환과 데이터그램 패킷 교환은 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/Network/#가상회선-패킷-교환과-데이터그램-패킷-교환은-무엇인가요)
        * [3-way 핸드셰이크와 4-way 핸드셰이크를 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/Network/#3-way-핸드셰이크와-4-way-핸드셰이크를-설명해-주세요)
            + [3-way Handshake에서 서버도 클라이언트의 ACK 패킷을 기다리는 이유는 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/Network/#3-way-handshake에서-서버도-클라이언트의-ack-패킷을-기다리는-이유는-무엇인가요)
        * [SYN Flooding이 무엇이며 이를 방어하는 방법은 무엇입니까?](https://github.com/tini-min/Tech-Interview/tree/master/Network/#syn-flooding이-무엇이며-이를-방어하는-방법은-무엇입니까)
        * [TCP 연결이 수립되고 실제로 데이터를 보내는 방식을 설명하고 이를 효율적으로 하기 위해서 제안된 방식이 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/Network/#tcp-연결이-수립되고-실제로-데이터를-보내는-방식을-설명하고-이를-효율적으로-하기-위해서-제안된-방식이-무엇인가요)
        * [TCP에서 흐름제어와 혼잡제어가 무엇입니까?](https://github.com/tini-min/Tech-Interview/tree/master/Network/#tcp에서-흐름제어와-혼잡제어가-무엇입니까)
    - [TCP/IP(Transmission Control Protocol / Internet Protocol) 모델이 무엇입니까?](https://github.com/tini-min/Tech-Interview/tree/master/Network/tcpiptransmission-control-protocol--internet-protocol-모델이-무엇입니까)
    - [HTTP와 HTTPS는 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/Network/#http와-https는-무엇인가요)
        * [SSL의 동작 방식을 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/Network/#ssl의-동작-방식을-설명해-주세요)
        * [단방향 암호화와 양방향 암호화는 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/Network/#단방향-암호화와-양방향-암호화는-무엇인가요)
            + [대칭키와 공개키는 무엇입니까?](https://github.com/tini-min/Tech-Interview/tree/master/Network/#대칭키와-공개키는-무엇입니까)
            + [암호화 키를 비공개하고 복호화 키를 공개하는 경우에 대해 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/Network/#암호화-키를-비공개하고-복호화-키를-공개하는-경우에-대해-설명해-주세요)
        * [HTTP의 GET과 POST에 대해 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/Network/#http의-get과-post에-대해-설명해-주세요)
        * [조회에 POST보다 GET이 사용되는 이유는 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/Network/#조회에-post보다-get이-사용되는-이유는-무엇인가요)
        * [HTTP Method에서 POST과 PATCH의 차이점을 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/Network/#http-method에서-post과-patch의-차이점을-설명해-주세요)
        * [쿠키와 세션이 무엇이며, 필요한 이유가 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/Network/#쿠키와-세션이-무엇이며-필요한-이유가-무엇인가요)
    - [소켓 프로그래밍이란 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/Network/#소켓-프로그래밍이란-무엇인가요)
        * [클라이언트 소켓과 서버 소켓이 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/Network/#클라이언트-소켓과-서버-소켓이-무엇인가요)
        * [소켓 API의 실행 흐름에 대해서 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/Network/#소켓-api의-실행-흐름에-대해서-설명해-주세요)
        * [HTTP 통신과 소켓 통신의 장단점을 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/Network/#http-통신과-소켓-통신의-장단점을-설명해-주세요)
    - [웹 브라우저에 URL을 입력하면 일어나는 시나리오에 대해 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/Network/#웹-브라우저에-url을-입력하면-일어나는-시나리오에-대해-설명해-주세요)
        * [DNS 동작 방식을 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/Network/#dns-동작-방식을-설명해-주세요)
        * [프록시 서버란 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/Network/#프록시-서버란-무엇인가요)
    - [웹 서버와 웹 애플리케이션 서버란 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/Network/#웹-서버와-웹-애플리케이션-서버란-무엇인가요)
    - [네트워크 바이트 오더가 무엇입니까?](https://github.com/tini-min/Tech-Interview/tree/master/Network/#네트워크-바이트-오더가-무엇입니까)
        * [빅엔디안과 리틀엔디안이 무엇이고, 각각의 장단점은 무엇입니까?](https://github.com/tini-min/Tech-Interview/tree/master/Network/#빅엔디안과-리틀엔디안이-무엇이고-각각의-장단점은-무엇입니까)
    - [로드 밸런싱이 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/Network/#로드-밸런싱이-무엇인가요)
        * [로드 밸런서가 서버를 선택하는 방식을 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/Network/#로드-밸런서가-서버를-선택하는-방식을-설명해-주세요)
        * [L4 로드 밸런서와 L7 로드 밸런서에 대해 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/Network/#l4-로드-밸런서와-l7-로드-밸런서에-대해-설명해-주세요)
    - [REST(REpresentational State Transfer)란 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/Network/#restrepresentational-state-transfer란-무엇인가요)
        * [REST의 특징을 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/Network/#rest의-특징을-설명해-주세요)
        * [RESTful API란 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/Network/#restful-api-무엇인가요)

    </div>
    </details>

1. [Database](https://github.com/tini-min/Tech-Interview/tree/master/DB/)

    <details>
    <summary><strong>목차</strong></summary>
    <div markdown = "1">

    - [데이터베이스의 정의는 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/DB/#데이터베이스의-정의는-무엇인가요)
        * [데이터베이스의 특징은 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/DB/#데이터베이스의-특징은-무엇인가요)
    - [인데스는 무엇입니까?](https://github.com/tini-min/Tech-Interview/tree/master/DB/#인데스는-무엇입니까)
        * [DBMS의 인덱스는 어떤 알고리즘으로 관리되나요?](https://github.com/tini-min/Tech-Interview/tree/master/DB/#dbms의-인덱스는-어떤-알고리즘으로-관리되나요)
            + [해시 인덱스가 사용되는 예시를 들어주세요.](https://github.com/tini-min/Tech-Interview/tree/master/DB/#해시-인덱스가-사용되는-예시를-들어주세요)
        * [인덱스 생성에 해시 알고리즘 보다 B-알고리즘이 사용되는 이유가 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/DB/#인덱스-생성에-해시-알고리즘-보다-b-알고리즘이-사용되는-이유가-무엇인가요)
        * [DML이 자주 일어나는 경우 인덱스를 사용하면 어떻게 되나요?](https://github.com/tini-min/Tech-Interview/tree/master/DB/#dml이-자주-일어나는-경우-인덱스를-사용하면-어떻게-되나요)
        * [클러스터드 인덱스와 넌클러스터드 인덱스가 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/DB/#클러스터드-인덱스와-넌클러스터드-인덱스가-무엇인가요)
            + [프라이머리 인덱스와 클러스터드 인덱스의 차이점은 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/DB/#프라이머리-인덱스와-클러스터드-인덱스의-차이점은-무엇인가요)
        * [Composite Index란 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/DB/#composite-index란-무엇인가요)
    - [키의 종류를 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/DB/#키의-종류를-설명해-주세요)
    - [정규화란 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/DB/#정규화란-무엇인가요)
        * [정규화의 종류를 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/DB/#정규화의-종류를-설명해-주세요)
        * [이상 현상에 대해서 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/DB/#이상-현상에-대해서-설명해-주세요)
        * [정규화의 장단점과 단점에 대한 대응책은 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/DB/#정규화의-장단점과-단점에-대한-대응책은-무엇인가요)
    - [트랜잭션이 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/DB/#트랜잭션이-무엇인가요)
        * [트랜잭션 격리 수준이 뭔가요?](https://github.com/tini-min/Tech-Interview/tree/master/DB/#트랜잭션-격리-수준이-뭔가요)
        * [트랜잭션 격리성 관련 문제점들은 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/DB/#트랜잭션-격리성-관련-문제점들은-무엇인가요)
        * [트랜잭션 로킹(Locking)이 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/DB/#트랜잭션-로킹locking이-무엇인가요)
    - [SQL injection에 대해 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/DB/#sql-injection에-대해-설명해-주세요)
        * [SQL injection을 방어할 수 있는 방법들을 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/DB/#sql-injection을-방어할-수-있는-방법들을-설명해-주세요)
        * [Statement vs PreparedStatement](https://github.com/tini-min/Tech-Interview/tree/master/DB/#statement-vs-preparedstatement)
    - [CHAR와 VARCHAR의 차이는 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/DB/#char와-varchar의-차이는-무엇인가요)
    - [NoSQL이 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/DB/#nosql이-무엇인가요)

    </div>
    </details>

1. [Computer Architecture](https://github.com/tini-min/Tech-Interview/tree/master/ComputerArchitecture/)

    <details>
    <summary><strong>목차</strong></summary>
    <div markdown = "1">

    - [하드웨어의 구성에 대해 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/ComputerArchitecture/#하드웨어의-구성에-대해-설명해-주세요)
        * [RAM에서 Random이 의미하는 바가 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/ComputerArchitecture/#ram에서-random이-의미하는-바가-무엇인가요)
        * [SSD와 HDD의 차이점은?](https://github.com/tini-min/Tech-Interview/tree/master/ComputerArchitecture/#ssd와-hdd의-차이점은)
        * [시스템 버스는 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/ComputerArchitecture/#시스템-버스는-무엇인가요)
    - [CPU의 동작은 어떤 과정으로 이뤄지나요?](https://github.com/tini-min/Tech-Interview/tree/master/ComputerArchitecture/#cpu의-동작은-어떤-과정으로-이뤄지나요)
        * [명렁어 사이클이 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/ComputerArchitecture/#명렁어-사이클이-무엇인가요)
        * [인출 사이클과 실행 사이클에 의한 명령어 처리과정에 대해 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/ComputerArchitecture/#인출-사이클과-실행-사이클에-의한-명령어-처리과정에-대해-설명해-주세요)
        * [간접 사이클과 인터럽트 사이클에 의한 명령어 처리과정에 대해 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/ComputerArchitecture/#간접-사이클과-인터럽트-사이클에-의한-명령어-처리과정에-대해-설명해-주세요)
    - [파이프라이닝이 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/ComputerArchitecture/#파이프라이닝이-무엇인가요)
        * [파이프라인 해저드가 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/ComputerArchitecture/#파이프라인-해저드가-무엇인가요)
        * [파이프라인 해저드를 해결하기 위한 방안은 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/ComputerArchitecture/#파이프라인-해저드를-해결하기-위한-방안은-무엇인가요)
    - [캐시 메모리는 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/ComputerArchitecture/#캐시-메모리는-무엇인가요)
        * [캐시 메모리의 작동 원리에 대해 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/ComputerArchitecture/#캐시-메모리의-작동-원리에-대해-설명해-주세요)
        * [Cache Miss의 종류 3가지에 대해 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/ComputerArchitecture/#Cache-Miss의-종류-3가지에-대해-설명해-주세요)
        * [캐시 메모리에서 사상이 무엇이고 사상 방식에 대해 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/ComputerArchitecture/#캐시-메모리에서-사상이-무엇이고-사상-방식에-대해-설명해-주세요)
        * [캐시 메모리의 데이터가 업데이트 되었을 경우 취할 수 있는 방법에 대해서 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/ComputerArchitecture/#캐시-메모리의-데이터가-업데이트-되었을-경우-취할-수-있는-방법에-대해서-설명해-주세요)
    - [해밍코드 생성 및 해석 해보기](https://github.com/tini-min/Tech-Interview/tree/master/ComputerArchitecture/#해밍코드-생성-및-해석-해보기)
    - [보수를 사용하는 이유가 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/ComputerArchitecture/#보수를-사용하는-이유가-무엇인가요)
        * [1의 보수와 2의 보수를 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/ComputerArchitecture/#1의-보수와-2의-보수를-설명해-주세요)
    - [ARM 프로세서는 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/ComputerArchitecture/#arm-프로세서는-무엇인가요)
        * [CISC와 RISC의 장단점은 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/ComputerArchitecture/#CISC와-RISC의-장단점은-무엇인가요)

    </div>
    </details>

1. [Software Engineering](https://github.com/tini-min/Tech-Interview/tree/master/SoftwareEngineering/)

    <details>
    <summary><strong>목차</strong></summary>
    <div markdown = "1">

    - [TDD란 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/SoftwareEngineering/#tdd란-무엇인가요)
    - [애자일(Agile)이 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/SoftwareEngineering/#애자일agile이-무엇인가요)
        * [스크럼이 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/SoftwareEngineering/#스크럼이-무엇인가요)
        * [데브옵스가 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/SoftwareEngineering/#데브옵스가-무엇인가요)
    - [객체지향 프로그래밍이 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/SoftwareEngineering/#객체지향-프로그래밍이-무엇인가요)
        * [OOP의 특징은 무엇이 있나요?](https://github.com/tini-min/Tech-Interview/tree/master/SoftwareEngineering/#OOP의-특징은-무엇이-있나요)
            + [오버라이딩과 오버로딩을 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/SoftwareEngineering/#오버라이딩과-오버로딩을-설명해-주세요)
        * [객체 지향 설계 원칙에 대해 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/SoftwareEngineering/#객체-지향-설계-원칙에-대해-설명해-주세요)
    - [함수형 프로그램밍이 무엇입니까?](https://github.com/tini-min/Tech-Interview/tree/master/SoftwareEngineering/#함수형-프로그램밍이-무엇입니까)
        * [객체 지향 프로그래밍과 함수형 프로그래밍의 차이는 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/SoftwareEngineering/#객체-지향-프로그래밍과-함수형-프로그래밍의-차이는-무엇인가요)
    - [프레임워크가 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/SoftwareEngineering/#프레임워크가-무엇인가요)

    </div>
    </details>

1. [Data Structure](https://github.com/tini-min/Tech-Interview/tree/master/DataStructure/)

    <details>
    <summary><strong>목차</strong></summary>
    <div markdown = "1">

    - [Linked List를 사용하는 이유는?](https://github.com/tini-min/Tech-Interview/tree/master/DataStructure/#linked-list를-사용하는-이유는)
    - [Heap의 삽입과 삭제 구현 방법은?](https://github.com/tini-min/Tech-Interview/tree/master/DataStructure/#heap의-삽입과-삭제-구현-방법은)
    - [BST의 문제점은 무엇이 있나요?](https://github.com/tini-min/Tech-Interview/tree/master/DataStructure/#bst의-문제점은-무엇이-있나요)
    - [AVL Tree와 Red-Black Tree가 무엇입니까?](https://github.com/tini-min/Tech-Interview/tree/master/DataStructure/#avl-tree와-red-black-tree가-무엇입니까)
    - [해시에 대해 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/DataStructure/#해시에-대해-설명해-주세요)
        * [해시의 충돌 현상을 해결할 수 있는 방법이 어떤 것들이 있나요?](https://github.com/tini-min/Tech-Interview/tree/master/DataStructure/#해시의-충돌-현상을-해결할-수-있는-방법이-어떤-것들이-있나요)

    </div>
    </details>

1. [Algorithm](https://github.com/tini-min/Tech-Interview/tree/master/Algorithm/)

    <details>
    <summary><strong>목차</strong></summary>
    <div>

    - [DFS와 BFS의 특징 및 차이점은?](https://github.com/tini-min/Tech-Interview/tree/master/Algorithm/#dfs와-bfs의-특징-및-차이점은)
    - [피보나치 수를 구하는 함수를 다이나믹 프로그래밍으로 구현할 때, 탑 다운 방식과 바텀 업 방식이 무엇이고 또한, 이를 어떻게 구현할 수 있습니까?](https://github.com/tini-min/Tech-Interview/tree/master/Algorithm/#피보나치-수를-구하는-함수를-다이나믹-프로그래밍으로-구현할-때-탑-다운-방식과-바텀-업-방식이-무엇이고-또한-이를-어떻게-구현할-수-있습니까)
    - [정렬 알고리즘의 종류와 특징을 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/Algorithm/#정렬-알고리즘의-종류와-특징을-설명해-주세요)
        * [삽입 정렬의 최선의 경우, 퀵 정렬의 최악의 경우를 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/Algorithm/#삽입-정렬의-최선의-경우-퀵-정렬의-최악의-경우를-설명해-주세요)
    - [MST 알고리즘 중 Kruskal 알고리즘과 Prim 알고리즘을 설명하고 장단점을 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/Algorithm/#mst-알고리즘-중-kruskal-알고리즘과-prim-알고리즘을-설명하고-장단점을-설명해-주세요)

    </div>
    </details>

    [손코딩 예상 문제 및 예제 답안](https://github.com/tini-min/Tech-Interview/tree/master/Algorithm/손코딩/)

1. [Language](https://github.com/tini-min/Tech-Interview/tree/master/Language/)

    <details>
    <summary><strong>언어 목록</strong></summary>
    <div markdown = "1">

    - [C](https://github.com/tini-min/Tech-Interview/tree/master/Language/C/)
        <details>
        <summary><strong>목차</strong></summary>
        <div>

        - [C언어의 특징을 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/Language/C/#c언어의-특징을-설명해-주세요)

        </div>
        </details>
    - [CPP](https://github.com/tini-min/Tech-Interview/tree/master/Language/CPP/)
        <details>
        <summary><strong>목차</strong></summary>
        <div>

        - [C++언어의 특징을 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/Language/CPP/#c언어의-특징을-설명해-주세요)

        </div>
        </details>
    - [JAVA](https://github.com/tini-min/Tech-Interview/tree/master/Language/JAVA/)
        <details>
        <summary><strong>목차</strong></summary>
        <div>

        - [Java 언어의 특징을 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/Language/JAVA/#java-언어의-특징을-설명해-주세요)
        - [static에 대해서 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/Language/JAVA/#static에-대해서-설명해-주세요)

        </div>
        </details>
    - [Python](https://github.com/tini-min/Tech-Interview/tree/master/Language/Python/)
        <details>
        <summary><strong>목차</strong></summary>
        <div>

        - [파이썬의 특징을 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/Language/Python/#파이썬의-특징을-설명해-주세요)
            * [컴파일 언어와 인터프리터 언어의 차이점은 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/Language/Python/#컴파일-언어와-인터프리터-언어의-차이점은-무엇인가요)
            * [.pyc파일과 .py파일이 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/Language/Python/#pyc파일과-py파일이-무엇인가요)
        - [mutuable과 immutuable에 대해 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/Language/Python/#mutuable과-immutuable에-대해-설명해-주세요)
        - [파이썬의 삼항연산자에 대해 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/Language/Python/#파이썬의-삼항연산자에-대해-설명해-주세요)
        - [아래 Switch 구문을 파이썬으로 구현해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/Language/Python/#아래-switch-구문을-파이썬으로-구현해-주세요)

            <details>
            <summary><strong>목차</strong></summary>
            <div>

            ```cpp
            using namespace std;

            // Function to convert number into string
            string numbers_to_strings(int argument){
                switch(argument) {
                    case 0:
                        return "zero";
                    case 1:
                        return "one";
                    case 2:
                        return "two";
                    default:
                        return "nothing";
                };
            };

            int main()
            {
                int argument = 0;
                cout << numbers_to_strings(argument);
                return 0;
            }
            ```

            </div>
            </details>

        </div>
        </details>

    </div>
    </details>

1. [Android](https://github.com/tini-min/Tech-Interview/tree/master/Android/)
    <details>
    <summary><strong>목차</strong></summary>
    <div markdown = "1">

    - [안드로이드의 4대 구성요소가 무엇인가요?](https://github.com/tini-min/Tech-Interview/tree/master/Android/#안드로이드의-4대-구성요소가-무엇인가요)
    - [Activity의 생명주기가 무엇이가요?](https://github.com/tini-min/Tech-Interview/tree/master/Android/#activity의-생명주기가-무엇이가요)
    - [스레드, 핸들러, 루퍼 예제](#스레드-핸들러-루퍼-예제)
    - [콜백(Callback)과 리스너(Listener)에 대해서 설명해 주세요.](https://github.com/tini-min/Tech-Interview/tree/master/Android/#콜백callback과-리스너listener에-대해서-설명해-주세요)

    </div>
    </details>

1. [인성면접 대비](https://github.com/tini-min/Tech-Interview/tree/master/인성면접/)

---
# Reference

* [JaeYeopHan 님의 Interview_Question_for_Beginner](https://github.com/JaeYeopHan/Interview_Question_for_Beginner)
* [Gyeseok Kim 님의 Tech Interview for developer](https://gyoogle.dev/blog/)
* [WeareSoft 님의 tech-interview](https://github.com/WeareSoft/tech-interview)