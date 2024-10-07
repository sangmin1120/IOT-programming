# IOT-programming
-------------------------------------------------

- 실습 환경 : STM32 IDLE
- Nucleo-F446RE , Rora board
  
- branch에 week 과정 작성 , VERSION을 define해서 # 실습 번호로 설정 

## week4 : 타이머 사용 및 내부 인터럽트
----------------------------------------------------
- 내부 인터럽트 설정 ( 내부 타이머 ) : Clock Configuration 설정 -> Timers > TIM2 ( Prescalar , Counter Register ) 설정 -> 인터럽트 사용

-  stm32f4xx_hal_tim.c에 정의되어 있는 내부 함수

- HAL_TIM_Base_Start_IT(TIM_HandleTypeDef *htim)
	- 타이머를 시작하도록 한다.
	- while 전에 작성해 주면 된다.

- HAL_TIM_PeriodElapsedCallback(TIM_HandleTypeDef *htim)
	- Timer에서 내부 인터럽트가 발생하면 실행되는 함수
	- prescalar , counter 값에 따라 callback 함수를 정의하면 된다.


1. 실습 1 : 5초에 한번씩 state가 변하는 신호등
	state 0 : LD2 off
	state 1 : LD2 on
	state 2 : LD2 점멸 신홍 ( toggle )
=> VERSION 1 : 내부 타이머의 신호가 올 때마다 state 값을 변경해주면된다.

2. 실습 2 : B1을 사용하여 B1이 한 번 눌리면 현재 상태 그대로 머물러 있고 ,
		다시 누르면 신호등 동작을 재개
=> VERSION 2 : VERSION 1  + B1 인터럽트를 이용해 버튼 동작에 따라 state값을 유지 시켜주면 된다.
