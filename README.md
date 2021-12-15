# My_lora_test
   ############在其它地方引用或转载请标明本文网址出处########
1.硬件：
野火f103mini开发板

lora模块（正点原子ATK-LORA-V3.0）两个

USB转ttl线一条

dht11温度湿度传感器一个

ps:由于野火的mini开发板和正点原子的略有不同，移植时原子的例程程序是无法使用的，原子的例程里使用了lcd屏因此还需要附带设置flash，sd卡等。由于

lcd是引脚大户而野火和原子的stm32的lcd所接的引脚不同，修改起来工作量很大。便删除了液晶屏以及相关程序，使用串口来输出显示发送和接收的内容。

2.硬件接线：


1.连接开发板的lora：MD0接PB8,AUX接PB9,RXD接PB10,TXD接PB11,gnd接地，vcc接5v

2.连接ttl的lora：MD0接地,AUX接地,RXD接usb转ttl线的TXD,TXD接usb转ttl线的RXD,gnd接地，vcc接5v。

3.dht11与板子的连接方式看下图



3.执行过程图片以及视频
 1.单电脑双usb口。单片机上的lora和usb转ttl的lora分别插在电脑上的两个不同的usb口，一个lora发送一个lora接受

测试时可以看见com5和com3两个口都接收到了传输的温度湿度数据



完整视频见https://www.bilibili.com/video/BV1E54y117RG?p=1

2.双电脑。单片机上的lora和usb转ttl的lora分别插在不同的两台电脑上



可以看见两台不同的电脑的串口助手上都显示出了测得的温湿度。

 完整视频见https://www.bilibili.com/video/BV1bp4y1e7kd?p=2
