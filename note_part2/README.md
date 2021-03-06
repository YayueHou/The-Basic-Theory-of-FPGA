# FPGA的概要
## FPGA的构成要素
* 1.逻辑要素
* 2.I/O要素
* 3.布线要素(包括开关块、布线通道、连接块等)
## 可编程技术的实现
### 闪存
* 通过浮栅是否带电控制晶体管类型，带电为增强型，不带电为耗尽型
* 非易失，尺寸小，可重构，重构需高压
### 反熔丝
* 在多晶硅和布线层间插入ONO作为绝缘体，通过反熔丝环的导通控制通断
* 不可重构
### 静态存储器
* 两个CMOS反向器和两个PT传输晶体管实现。
* 根据地址信号驱动字线
* 大多应用查找表，使用数据选择器切换布线连接
* 漏电流相对较大，开关电容电阻相对较大
## FPGA逻辑实现
### 乘积项的实现
* 使用先AND再OR的方式，通过可编程开关控制输入内容在某个门的逻辑函数。
### 查找表
* 从上到下，数据始终在向下传输，输入信号的位置的晶体管会导通，数据只有在这条线上可以下行。
* 还可以用作存储器和移位寄存器使用，通过相位相反的移位控制信号来控制移位。
* 晶体管多，体积大
### 其他
* MUX目前已经被抛弃
