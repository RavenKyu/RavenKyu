# Hello World!
반가워요! <img src="https://raw.githubusercontent.com/aemmadi/aemmadi/master/wave.gif" width="30px">
웹디자이너로 시작하여 부족한 부분을 스스로 해결하려는 시도를 거듭하다 보니 어느새 개발자의 길을 걷고 있습니다. 훌륭한 코드는 아니지만 찾고자 하는 내용을 발견하시어 도움이 되길 바랍니다.

# Technologies
## Languages
* Python - Windows & Linux Application, Server Programing
* C - Linux Application, MCU Firmware, Linux Kernel Module
* ASM - AVR ASM
* Shell Script - Bash Script 
* JavsScript - ES6
* 그 외 낮은 숙련도 - Go, TypeScript

## DB
* SQLite
* InfluxDB
* MySQL
* PostgreSQL
* MongoDB
* REDIS

## Frameworks
### Python
* Flask 
* Django 
* SQLAlchemy 
* PyQt - Qt Binding for Python
* FastAPI 
* Celery 

### Javascript
* React
* Electron 
* Node.js

## 그 외
* Fluentd - Data Collector
* Docker

# Portfolio
## Embedded System Projects
### ARM 기반 데이터로거 
Python과 Extension C를 사용하여 데이터로거에 연결된 센서 데이터 수집, 저장, 설정용 웹서버 구현
Python AST를 활용하여 사용자 제공 언어를 구현하여 직접 코딩 가능한 범용 데이터로거 제작
* ARM11
* Embedded Linux Kernel 2.6
* Python3, C
* SQLite3
* Flask / Jinja2

### AVR 기반 데이터로거
* C 언어 사용
* ATmega2560으로 제작된 소형 데이터로거 
* RS282 시리얼통신을 통하여 설정이 가능한 CLI 제공
* 아날로그 센서 및 I2C, 시리얼 통신으로 센서 데이터 수집

### 용접 와이어 사용량 센서, 수집 모듈 - [RavenKyu/RotaryEncoderSensor](RavenKyu/RotaryEncoderSensor)
스마트팩토리 프로젝트로서 용접로봇에서 사용되는 용접와이어의 사용량을 기록하는 센서와 수집 서버 개발. 라즈베리파이로 시작하였으나 대량 생산을 고려하여 단순하게 TCP/IP Socket 통신과 자체 프로토콜 제작.
센서 동작시 로터리 엔코더 회전 길이 수집, 시간동기화, 시간보상, 미전송 데이터 보관
* 라즈베리파이 
* 로터리 엔코더
* Python
* SQLite
* TCP/IP Socket 통신

## Application
### Cliparse - CLI Framework - [https://github.com/RavenKyu/cliparse](https://github.com/RavenKyu/cliparse)
Python으로 손 쉽게 계층형 CLI Application 제작 가능
* Python의 `cmd` 모듈과 `argparse`를 기반

### MODBUS Command Line Client (Modbusclc) - [https://github.com/RavenKyu/modbus-command-line-client](https://github.com/RavenKyu/modbus-command-line-client)
자체제작 Python CLI Framework 인 `cliparse`를 사용하여 제작한 Modbus Client
* TCP/IP MODBUS 지원
* RTU over TCP/IP 지원
* ASCII 지원

### Data Collector
다양한 장치에서 요구하는 통신방법을 지원하여 데이터를 수집한다. 일정 간격 또는 원하는 날짜시간을 지정하여 동작을 수행할 수 있도록 설정이 가능하다. 모듈은 크게 `센서 데이터 수집`,  `데이터 수집`, `분산처리`, `데이터 저장`으로 나뉘어지며 `Docker Container`로 개별 실행된다. 모든 모듈은 개별 실행 가능.

* Python, Celery, Docker, Redis, InfluxDB, Fluentd, Grafana
* MODBUS, SNMP, RESTFul API, TCP/IP Socket

#### Restful MODBUS API - [https://github.com/RavenKyu/restful-modbus-api](https://github.com/RavenKyu/restful-modbus-api)
* TCP/IP MODBUS 프로토콜을 사용하는 다수의 장치에서 데이터 수집 
* Interval 또는 Cron 방식으로 수집 시간 지정
* Python Code를 사용하여 수집 방식 코딩 가능
* 수집 데이터는 RESTFul API로 제공

#### RESTFul SNMP API - [https://github.com/RavenKyu/restful-snmp-api](https://github.com/RavenKyu/restful-snmp-api)
* SNMP 프로토콜을 사용하는 다수의 장치에서 데이터 수집
* SNMP v1, v2 지원
* MIB 파일 지원
* Python Code를 사용하여 수집 방식 코딩 가능
* 수집된 데이터는 RESTFul API로 제공

#### Data Collector - [https://github.com/RavenKyu/data-collector](https://github.com/RavenKyu/data-collector)
`RESTful ... API` 모듈에서 데이터를 수집하여 Database에 넣거나 Event 처리

#### Celery Work Farm - [https://github.com/RavenKyu/celery-work-farm](https://github.com/RavenKyu/celery-work-farm)
Python Celery로 분산처리가 필요한 Task 처리

### RPA 
#### Python RPA Bot
Python 기반 RPA Bot 제작.
* 마우스 액션
* 키보드 입력, 단축키
* 이미지 매칭, OCR, 좌표찾기
* Selenium을 이용한 웹 브라우져 사용

