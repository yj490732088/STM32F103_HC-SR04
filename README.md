# STM32F103_HC-SR04

多个超声波模块测量程序

## EXTI

### 1. 轮询测量（Polling）

**对应的工程：**==STM32F103_HC-SR04_EXTI_Polling==

通过轮询方式依次测量距离值。

**注意：**

1. 外部中断触发方式选择**上升沿触发（EXIT_Trigger_Rising）**
2. 根据手册，测量周期≥60ms（此处周期是指多个的测量周期，该周期等于各个模块测量周期之和）

- 优点：
- 缺点：

### 2. 同步测量

**对应的工程：**==STM32F103_HC-SR04_EXTI_Synchronization==

通过类似与时间片的方式测量距离值

**注意：**

1. 外部中断触发方式选择**上升沿下降沿都触发（EXTI_Trigger_Rising_Falling）**
2. 根据手册，测量周期≥60ms（此处单个测量周期和多个的周期是一致的）

- 优点：
- 缺点：