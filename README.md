# IOT-programming
-------------------------------------------------

- 실습 환경 : STM32 IDLE
- Nucleo-F446RE , Rora board
- 
- branch에 week 과정 작성 , VERSION을 define해서 # 실습 번호로 설정 

  ## week1 : 실습 환경 준비

  ## week2 : HAL_GPIO_WritePin 으로 LD2 제어

  ## week3 : HAL_GPIO_ReadPin 으로 B1 버튼 스위치 제어 , 인터럽트로 스위치 입력
  ------------------------------------------------------
  - B1 버튼 스위치 설정 ( 폴링 ) : Datasheet 확인 -> PC13과 B1 연결 확인 -> 핀 설정 -> HAL_GPIO_ReadPin으로 스위치 상태 받기
  - 인터럽트로 스위치 입력 : NVIC 에서 인터럽트 활성화 -> main에서 인터럽트 초기화 , 인터럽트 핸들러 작성
 
  - 폴링 : 우선 순위가 없는 순차적 처리 방식
  - 인터럽트 : 우선 순위가 높은 코드를 먼저 처리하는 방식
 
  1. 실습1 : 스위치를 누르고 있을 때 , 0.5초 간격으로 LED 깜박이고
              스위치에서 손을 떼었을 때 LED꺼지는 동작 
  2. 실습2 : B1 스위치를 누르면 0.5초 깜빡이고
              다시 누르면 LDE 상태로 멈춰있도록 동작

  ## week4 : 타이머 사용 및 내부 인터럽트
  -------------------------------------------------
