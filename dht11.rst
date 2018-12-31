使用pyboard读取dht11温湿度传感器信息
=====================================
模块介绍
------------------
DHT11是一款有已校准数字信号输出的温湿度传感器。其精度湿度+-5%RH，温度+-2℃，量程湿度20-90%RH，温度0~50℃。下面详细讲解使用pyboard读取dht11温湿度传感器信息的过程。

.. image:: https://github.com/tian0927/hello-world/raw/master/ws00.jpg

编程学习
------------------
在main.py中编写函数读取温湿度数值
引入库函数：

.. image:: https://github.com/tian0927/hello-world/raw/master/ws4.png

定义DHT11类，初始化引脚：

.. image:: https://github.com/tian0927/hello-world/raw/master/ws5.png

读温度函数，按照时序设置引脚电平高低：

.. image:: https://github.com/tian0927/hello-world/raw/master/ws6.png

将引脚设置成输入模式，等待温度传感器响应：

.. image:: https://github.com/tian0927/hello-world/raw/master/ws7.png

通过引脚接收数据：

.. image:: https://github.com/tian0927/hello-world/raw/master/ws8.png

利用接收的电平信号算出温湿度数值：

.. image:: https://github.com/tian0927/hello-world/raw/master/ws9.png

将X4引脚传入DHT11类循环测量温湿度数值：

.. image:: https://github.com/tian0927/hello-world/raw/master/ws10.png

实验现象
------------------
按RST按键重启pyboard，加载程序。打开终端输入sudo picocom /dev/ttyACM0命令，就可看到读取的温湿度数值

.. image:: https://github.com/tian0927/hello-world/raw/master/ws11.png


