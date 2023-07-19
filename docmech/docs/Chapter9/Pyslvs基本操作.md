# 9.1.1 Pyslvs基本操作

## 简介
&emsp;&emsp;**Pyslvs**是一个开源的平面联动机构仿真和机械合成系统，它的名字来自“Python”和“Solvers”。简单来说，这是一个简单的**2D连杆机构运动仿真界面**。有很多其他的软件可以实现运动仿真，比如建模软件Solidworks以及多体动力学仿真软件Adams。区别在于，这款软件构建的连杆机构仅仅是简图，而非实体，可以节约时间。界面中设置完Joints和Links后可以通过手动拖动或者设置马达驱动以观察**输出点在平面中形成的曲线**。

<center>
    <img src = "https://raw.githubusercontent.com/Ostoponko/Picstorage/master/img/main-win.png"
    width="60%">
    <br>PMKS仿真软件界面
</center>


>官方文档：https://pyslvs-ui.readthedocs.io/en/latest/

&emsp;&emsp;Pyslvs参考了俄勒冈州州立大学Matthew I. Campbell的项目[PMKS(Planar Mechanism Kinematic Simulator)](https://designengrlab.github.io/PMKS/)。

<center>
    <img src = "https://raw.githubusercontent.com/Ostoponko/Picstorage/master/img/pmks-example.png"
    width="40%">
    <br>PMKS仿真软件界面
</center>

## 软件界面

<center>
    <img src = "https://raw.githubusercontent.com/Ostoponko/Picstorage/master/img/pyslvs2.png"
    width="50%">
    <br>Mechanism界面
</center>

+ **Mechanism界面**：可设置运动副坐标（JoInts）位置，运动副是否接地（固连至机架）。框选运动副可设置连杆（Links）。这是机构简图绘制的主界面；

+ **Inputs界面**：可以设置原动件，观察输出点轨迹，获取输出点位置速度图像；

+ **Synthesis界面**：用于机构综合，帮助用户重建机构；

+ **Project界面**：用于设置保存路径以及另存为其他格式。

## 基本操作

>Step1: 建立运动副和连杆。运动副可设置是否grounded(固连机架)。

<center>
    <img src = "https://raw.githubusercontent.com/Ostoponko/Picstorage/master/img/pyslvs1.png"
    width="50%">
    <br>建立运动副，设置连杆
</center>

>Step2: 设置机构输入（原动件）可观察原动件和输出的运动轨迹。

<center>
    <img src = "https://raw.githubusercontent.com/Ostoponko/Picstorage/master/img/pyslvs3.png"
    width="40%">
    <img src = "https://raw.githubusercontent.com/Ostoponko/Picstorage/master/img/pyslvs4.png"
    width="40%">
    <br>设置原动件，观察输出轨迹以及位置、速度曲线
</center>




