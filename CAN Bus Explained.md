## CAN Bus Explained

> **CAN bus definition:**
>
>  If the car is like human body, the CAN Bus System is like the nervous System,  facilitating communication between  all part of the body.
>
> Similarly, electronic control units ECU are connected via the CAN bus. 
>
> The primary function of CAN:
>
> To allow any ECU to communicate with the entire system without causing an overload to the  controller computer



现代的汽车可能为其子系统配备多达70个[电子控制器](https://zh.wikipedia.org/wiki/电子控制器)（ECU）。最常见的控制器为[发动机控制器](https://zh.wikipedia.org/wiki/发动机控制器)。除此以外，[变速器](https://zh.wikipedia.org/wiki/傳動輪)、[安全气囊](https://zh.wikipedia.org/wiki/安全气囊)、[防抱死制动系统](https://zh.wikipedia.org/wiki/防鎖死煞車系統)/ABS、[定速巡航](https://zh.wikipedia.org/wiki/巡航定速)、[动力方向盘](https://zh.wikipedia.org/wiki/動力方向盤)、音响系统、[动力车窗](https://zh.wikipedia.org/w/index.php?title=动力车窗&action=edit&redlink=1)、车门、后视镜调整、电池和混合动力电动汽车的充电系统等等均使用电子控制器。这其中，有的是独立的子系统，有些需要跟其他子系统进行通信，控制驱动器或接收传感器的反馈信息。为此设计了控制器局域网络，将汽车的不同系统相互连接在一起。传统的“电缆直连”成本高，布线复杂，而控制器局域网络仅需软件就可实现，不仅安全、经济还十分便利。



> **What does A CAN message look like?**
>
> The 8 key parts of a CAN message are as follow:
>
> 1 bit: SOF (start of frame) is a 'dominant 0' to tell the other ECUs that a message is coming
>
> 29 bit: CAN ID: contains the message priority as well as functional address.(RPM, wheel speed...)
>
> 1 bit: RTR: The remote transmission request allows ECUs to request messages from other ECUs
>
> 6 bit: Control: Informs the length of the Data in bytes.
>
> 0-64 bit: Data: contains the actual data values, which need to be scaled or converted to be readable and ready for analysis
>
> 16 bit: CRC: The Cyclic Redundancy Check: checks data integrity 
>
> 2 bit: ACK: The ACK slot indicate if the CRC process is OK
>
> 7 bit: EOF: marks the end of the CAN message

![image-20201109081319342](C:\Users\wangz\AppData\Roaming\Typora\typora-user-images\image-20201109081319342.png)

[![Car data from the CAN bus – Tauvic's Blog](https://tauvicr.files.wordpress.com/2019/07/canbus_network.png)966 × 593](https://www.google.com/url?sa=i&url=https%3A%2F%2Ftauvicr.wordpress.com%2F2019%2F07%2F05%2Freading-car-data-from-the-can-bus%2F&psig=AOvVaw2nDDmVUHhiUM5rbnfo7RiC&ust=1605014098718000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCPC9gM3F9ewCFQAAAAAdAAAAABAW)

The most important: CAN ID - Control - Data field

Usually see them in CAN Bus data output



