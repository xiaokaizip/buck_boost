# TODO - RM SuperCap Controller V2.1

当前项目后续开发待办项：

## 1. 软件数据流设计
- 绘制模块间数据流图
- 确定每个模块输入/输出
- 确定 ADC -> PowerManager -> CurrentManager -> FSBB -> PWM 的路径

## 2. 模块接口(API)
- ChargeManager / DischargeManager
- PowerManager / VoltageManager / CurrentManager
- FaultManager
- CAN 接口
- Debug 接口

## 3. PWM Driver
- 接口定义：Enable / Disable / Update / BootstrapRefresh / Brake
- PWM 自举刷新策略确认
- PWM 输出占空比范围及死区管理

## 4. PI 参数
- Power PI / Voltage PI / Current PI
- 初始化参数及限幅
- 积分清零逻辑确认

## 5. ADC
- 滤波方法确认：IIR / 滑动平均
- 采样精度及分辨率确认
- 电流/电压零点校准

## 6. CAN
- 周期发送与接收
- TX/RX 数据结构确认
- 消息 ID、DLC、编码

## 7. FSBB 三模态
- Buck / Buck-Boost / Boost 边界确认
- Dg_base / Dg_comp / Dg_cmd 叠加规则
- 调制映射公式确认

## 8. FreeRTOS任务划分
- Task 划分：PowerTask / ChargeTask / DischargeTask / FaultTask / CANTask / DebugTask
- 优先级与频率

## 9. 调试接口
- ADC / Power / State / Fault / PWM 输出
- Debug 数据格式与周期

## 10. 测试计划
- 功率环调试流程
- 电流环调试流程
- FSBB 占空比验证
- 故障响应验证
- CAN 数据正确性验证
- PWM 自举刷新验证