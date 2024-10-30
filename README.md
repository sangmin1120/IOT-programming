# IOT-programming
-------------------------------------------------

- 실습 환경 : STM32 IDLE
- Nucleo-F446RE , Rora board
- 센서 : 근접 센서 , 진동 센서 , DHT11(온습도 센서)
  
- branch에 week 과정 작성 , VERSION을 define해서 # 실습 번호로 설정
- VERSION 1 : 근접 센서
- VRESION 2 : 진동 센서
- VERSION 3 : 온습도 센서

## week5 : 센서 정보 읽어오기
--------------------------------

1. UART 설정 : printf를 이용해 터미널로 출력한다.

- VERSION==1
  근접 센서 => PB13 번 핀을 사용해 입력 받아 출력한다. 근접하면 1 , 아무것도 없으면 0

- VERSION==2
