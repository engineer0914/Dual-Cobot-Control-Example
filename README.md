# Dual-Cobot-Control-Example
2대이상의 협동 로봇 설정을 위한 안내


## - 그리퍼 테스트

### RH P12 2핑거 그리퍼
https://github.com/engineer0914/arm_gripper_test/blob/main/test_cmd_serial.py

### GPIO 그리퍼
https://github.com/engineer0914/arm_gripper_test/blob/main/test_gpio_ctrl.py


## - 듀얼 동작을 위한 환경설정

### 1 로봇내 컨트롤 박스 TCP/IP 설정 필요

### RBapp -> setup -> Socket/Serial 탭 (버전별 상이)

A 로봇
* IP      : 10.0.2.7
* NETMASK : 255.255.255.0
* GATEWAY : NONE           <- 공백

B 로봇
* IP      : 10.0.2.8             <- A IP 제외
* NETMASK : 255.255.255.0   <- 동일
* GATEWAY : NONE           <- 공백

C 메인 우분투 PC
* IP      : 10.0.2.9             <- A,B IP 제외
* NETMASK : 255.255.255.0   <- 동일
* GATEWAY : NONE           <- 공백


### 2 이더넷 결선 구조

메인 PC ├─ 이더넷 허브/OR 와이파이 공유기
        │
        ├─ A 로봇팔
        │
        └─ B 로봇팔


### 3 듀얼 로봇을 위한 각개 IP 객체 선언
- 예제 참고

