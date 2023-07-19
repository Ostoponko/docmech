# 11.1 切片软件：Superslicer

## 何为切片
&emsp;&emsp;**[FDM](https://baike.baidu.com/item/%E7%86%94%E8%9E%8D%E6%B2%89%E7%A7%AF%E5%88%B6%E9%80%A0/9548501)**（熔融堆积式）3D打印最重要的技术实现就是将模型变成一层一层打印的路径，然后喷头末端的喷嘴以特定的速率走过这些路径，耗材从喷嘴中挤出，堆到预先规划好的路径之上，并在高温下形成与已打印部分的融合。切片操作的前置操作是将模型文件转换为**[STL](https://baike.baidu.com/item/stl%E6%A0%BC%E5%BC%8F)**(STereoLithography, 立体光刻)文件，这一步会将连续特征离散化，将曲面以特定的精度近似为一个一个小平面（比如一个外圆面会变成多边形面）。这一步就是为接下来切片软件的几何解析做准备。

>关于STL文件格式：[3D打印模型之STL文件](https://zhuanlan.zhihu.com/p/622392420)

&emsp;&emsp;切片软件的算法会分析模型的特征，根据3D打印的特性识别出**壁面、填充、搭桥**以及其他各种类型的打印部分，并生成合适的路径。除了构建零件本体之外，切片软件还会根据用户的需求在悬空部位生成特定模式的**支撑**；以及可以选择在零件底面与打印平台之间生成一层**裙边**，避免打印过程中由于内应力导致的收缩翘边。

<div align=center> <img src="https://ultimaker.cn/images/Step_3.png" width = 40%/> </div>

&emsp;&emsp;3D打印机需要执行的动作是热端三维坐标位置的移动，以及挤出机的进给动作。打印机的主控需要一段机器码，将其解算为电机的动作，再将需要执行的动作发送给电机，而这个机器码就是 **[G-code](https://baike.baidu.com/item/G%E4%BB%A3%E7%A0%81)**。一段G-code就描述了打印从头到尾的加工路径。切片软件在划分完不同特性的打印路径后，就会根据设置生成G-code代码。因此切片软件又叫做G-code generator。

&emsp;&emsp;当然，如果想要取得更完美的打印效果，就要根据零件特征、机器类型以及与耗材的实际情况进行切片的参数调整。常见的切片软件有Ultimaker厂家的Cura、Prusaslicer以及基于此的Superslicer。不同的切片软件有不同的切片算法、设置参数与特殊功能（如**自适应层高**等），但是对于简单零部件的打印来说，没有太大区别。

&emsp;&emsp;这里我们将以Superslicer为示例，讲一下如何操作。

## Superslicer

SuperSlicer takes 3D models (STL, OBJ, AMF) and converts them into G-code instructions for FFF printers or PNG layers for mSLA 3D printers. It's compatible with any modern printer based on the RepRap toolchain which is running a firmware based on Marlin, Prusa, Klipper, etc.

<div align=center> <img src="https://user-images.githubusercontent.com/6536403/85583872-ee45c980-b63e-11ea-89f6-c0b6cd838843.png" width = 40%/> </div>


SuperSlicer is based on PrusaSlicer by Prusa Research. PrusaSlicer is based on Slic3r by Alessandro Ranellucci and the RepRap community.

>官方Github：
<https://github.com/supermerill/SuperSlicer>

## Ss软件基本设置

+ **Step1**: 初次进入Superslicer软件后，会出现快速配置界面，目的是为了适配用户个人的打印机。在这里选择我的打印机型号：Voron v2 Afterburner系列的300mm尺寸机器，默认使用0.4mm喷嘴。 选择之后系统便会出现Voron机器300mm尺寸大小的打印平台。我们的切片将在这个平面上进行操作。当模型超出平台或尺寸超标时，模型都会变成红色，此时无法进行切片操作。只有模型是绿色时，才能进行接下来的操作。

<center>
    <img src = "https://raw.githubusercontent.com/Ostoponko/Picstorage/master/img/11.1.2.png"
    width= 50%">
</center>

+ **Step2**: 在设置里开启Expert选项，在打印机设置中确认G-code风格是否为Klipper。

<center>
    <img src = "https://raw.githubusercontent.com/Ostoponko/Picstorage/master/img/11.1.3.png"
    width= 40%">
</center>

+ **Step3**: 在材料设置里选择材料为PLA，参照耗材要求看温度是否合适。一般PLA的打印温度在180到220摄氏度之间，过低或过高的打印温度会造成一些问题，需要针对不同机器以及不同品牌的耗材进行实际测试，调整温度参数到合适区间。

<center>
    <img src = "https://raw.githubusercontent.com/Ostoponko/Picstorage/master/img/sssetting.png"
    width= 50%">
</center>

