# Router

## 라우터 IP설정

Q. ROUTER1의 fasteternet 0/0의 IP를 192.168.0.100/24로 설정하시오.

완료된 설정은 startup-config에 저장

```
>en		:시용자 모드에서 관리자 모드로 접속
>conf t		:관리자 모드에서 전역설정 모드로
>interface fastethernet 0/0		:라우터의 fastethernet 0/0 접속
>ip add 192.168.0.100 255.255.255.0		: ip추가하기 
>no shutdown		: 활성화 시키기
>exit			:종료
>exit
>copy r s		: 저장
```



> - **서브넷 마스크 /24의 의미**

> > 8비트씩 3개=> 24
> >
> > 11111111.11111111.11111111.00000000
> >
> > 255.255.255.0



## 라우터 대역폭 설정

Q. ROUTER2의 Serial 2/0의 대역폭을 2048로 설정하시오.

완료된 설정은 startup-config에 저장

```
>en
>conf t
>interface serial 2/0
>bandwidth 2048		: 대역폭 설정
>exit
>exit
>copy r s
```

Q. ROUTER1의 Serial 2/0의 클럭 속도를 72k로 설정하시오.

완료된 설정은 startup-config에 저장

```
>en
>conf t
>interface serial 2/0
>clock rate 72000		: 클럭속도 설정 k=1000
>exit
>exit
>copy r s
```



## 라우터 주석

 Q. fastethernet 0/0 의 Description을 설정하시오

Description: ICQA

```
>en
>conf t
>interface fastethernet 0/0
>description ICQA		:주석 달기
>exit
>exit
>copy r s
```



## 라우터 Secondary IP Address 설정

Q. ROUTER1의 Serial 2/0을 사용하게 IP주소를 192.168.0.101/24와 두번째 IP 192.168.0.102/24로 설정하고 활성화 하시오.

```
>en
>conf t
>interface serial 2/0
>ip add 192.168.0.101 255.255.255.0
>ip add 192.168.0.102 255.255.255.0 secondary		: 두번째 IP설정
>no shutdown
>exit
>exit
>copy r s
```



## 라우터 기본 게이트웨이 설정

Q. 기본 게이트웨이를 설정하시오.

IP : 192.168.0.10

```
>en
>conf t
>ip default-gateway 192.168.0.10		:기본 게이트웨이 설정
>exit
>copy r s
```

Q. ROUTER1의 DHCP네트워크를 192.168.100.0/24 서버이름은 'icqa'로 설정하시오

```
>en
>conf t
>ip dhcp pool icqa		:DHCP서버 이름 설정
>network 192.168.100.0 255.255.255.0		:네트워크 설정
>exit
>exit
>copy r s
```



## 텔넷 패스워드 설정

Q. ROUTER1 Telnet에 접근하는 Password를 icqa로 설정하고 로그인하세요.

```
>en
>conf t
>line vty 0 4		:텔넷 설정 명령어(가상터미널을 0~4까지 총 5개 사용하겠다는 의미)
>password icqa		:패스워드 설정 명령어
>login		:로그인
>exit
>exit
>copy r s
```



## 텔넷 세션 자동종료 설정

Q. 텔넷 연결 후 3분 50초 동안 입력이 없으면 세션이 자동 종료되도록 설정하시오.

```
>en
>conf t
>line vty 0 4
>exec-timeout 03 50
>exit
>exit
>copy r s
```



## 라우터 콘솔 패스워드 설정

Q. ROUTER1 console 0의 패스워드를 ICQA로 설정하고 로그인 하시오.

```
>en
>conf t
>line console 0		:콘솔 0으로 이동(console interface 명령어가 아니라 line명령어)
>password ICQA
>login
>exit
>exit
>copy r s
```



## 라우터 활성화 설정

Q. ROUTER1 Serial 2/0을 활성화시키시오.

```
>en
>conf t
>interface serial 2/0
>no shutdown
>exit
>exit
>copy r s
```



## 호스트 네임 설정

Q. ROUTER2의 호스트 이름을'ICQA'로 설정하시오.

```
>en
>conf t
>hostname ICQA		:호스트 네임 설정
>exit
>copy r s
```



Q. Hostname을 network2로 변경하고 console 0의 password를 route5로 변경 후 로그인 하시오.

```
>en
>conf t
>hostname network2
>line console 0
>password route5
>login
>exit
>exit
>copy r s
```



## 라우터 확인문제 유형 분석

Q. 인터페이스 정보를 확인하고 저장하시오.

```
>en
>show interface
>copy r s
```

Q. 접속한 사용자 정보를 확인하고 저장하시오.

```
>en
>show user
>copy r s
```

Q. 라우팅 테이블 정보를 확인하고 저장하시오.

```
 >en
 >show ip route
 >copy r s
```

Q. 플래쉬 내용을 확인하고 저장하시오.

```
>en
>show flash
>copy r s
```

Q. 프로세스 정보를 확인하고 저장하시오.

```
>en
>show process
>copy r s
```

