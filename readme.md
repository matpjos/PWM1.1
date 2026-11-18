updated from PWM1 --> PWM1.1(this)

Simple learning project PWM using timer-peripheral. Fades the on-board LED. 

*** logic pathway ***
1. TIM2 PWM enabled in STM32CubeMX
 
2. In CUbeIDE, enabling PWM Output: HAL_TIM_PWM_Start(&htim2, TIM_CHANNEL_1)

3. Software Fade Loop — a separate layer on top of PWM.
   step / HAL_Delay are not PWM parameters — they're application-level "rate of duty-cycle change," independent of PWM carrier frequency (PSC/ARR)