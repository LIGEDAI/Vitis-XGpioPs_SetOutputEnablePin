# XGpioPs_SetOutputEnablePin函数的用法
## 1.1定义
函数原型为`void XGpioPs_SetOutputEnablePin(const XGpioPs *InstancePtr, u32 Pin, u32 OpEnable){......}`作用是启用或禁用某个引脚（`u32 Pin`）作为输出。（`u32 OpEnable`为0则为禁用输出模式（引脚作为输入或其他功能），`u32 OpEnable`为1则为启用输出模式）
- `const XGpioPs *InstancePtr`为GPIO设备的驱动程序实例
- `u32 Pin`是对应的MIO接口
- `u32 OpEnable`设置引脚的输出使能状态
## 1.2实例
- `#define MIO_LED             0;`           //led连接到 MIO0
- `XGpioPs Gpio;`                //GPIO设备的驱动程序实例
- `XGpioPs_SetOutputEnablePin(&Gpio, MIO_LED, 1);`  //启用该引脚输出模式
