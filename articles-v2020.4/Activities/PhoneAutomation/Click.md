# 点击

点击移动设备上的界面元素。

注意：使用此组件时，请先连接设备，并将本组件放置在连接设备组件中。连接设备使用组件 [连接设备](ConnectPhone.md)。

## 属性
基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

目标
- **点击类型** ：执行点击的类型。有2种类型：单击，双击。


点击
- **光标位置** ：描述从 **横坐标偏移** 和 **纵坐标偏移** 属性添加偏移量的光标的起点。默认选项是**中心**
- **横坐标偏移** ：根据 **光标位置**字段中选择的选项，光标位置的水平位移像素量。例如填写“10”，则代表以**光标位置**为开始，向右偏移10个像素。计算坐标时，以屏幕左上角为原点。仅支持整型变量和整型
- **纵坐标偏移** ：根据**光标位置**字段中选择的选项，光标位置的垂直位移像素量。例如填写“10”，则代表以**光标位置**为开始，向下偏移10个像素。计算坐标时，以屏幕左上角为原点。仅支持整型变量和整型
- **横坐标百分比** ：根据**光标位置**进行百分比移动。以点击所指定矩形框的长度为基数，乘以此属性值，结果和 **光标位置**的横坐标相加，得到最终的点击横坐标。
例如填写"0.5",光标位置选择"中心"，最终点击位置的计算过程：取指定元素的矩形框长度，乘以0.5，结果为矩形框长度的一半；后和光标位置"中心"执行相加计算，最终得到的数字为点击的横坐标，即为矩形框的右边框中心处。