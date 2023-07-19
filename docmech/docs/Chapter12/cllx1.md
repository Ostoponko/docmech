# 12.1 材料力学基本概念

## 研究内容

&emsp;&emsp;与理论力学最直观的不同的是，完美刚体的假设不复存在了，正因此才会发生工程上桥梁坍塌、机械中螺栓弯曲的情况。我们将关注固体构件在收到外力时，内部产生的作用力，以及物体的形变。

<center>
<img src="https://raw.githubusercontent.com/Ostoponko/Picstorage/master/C7790DE9B6CF27F9B310FAF90104C6AD.png"
width="30%">
<br>步兵避震器安装螺栓的弯曲
</center>

&emsp;&emsp;研究材料力学，是为了确保在工程结构或机械当中的构件拥有足够的强度、刚度和稳定性，从而不至于在外力作用下发生结构破坏、大幅度形变以及脱离原平衡态，从而导致结构失效。这里提到了构件的三种基本特性：

+ **强度**：构件在外力作用下抵抗破坏的能力


+ **刚度**：构件在外力作用下抵抗变形的能力


+ **稳定性**：构件在外力作用下保持原有平衡形态的能力

## 基本假设

为了简化问题，我们也不得不做出一些假设，忽略物体的一些次要属性，从而把握我们所抽象模型的重点（这一步在任何理论建模的时候都是必要的）：

+ **连续性假设：组成固体的物质不留空隙地充满了固体的体积。** 事实上，组成物体的粒子之间有空隙，但是与构件尺寸相比过于微小。因此我们假设固体构建内部是连续的。


+ **均匀性假设：固体内部到处都有相同的力学性能。** 组成金属的各晶粒的力学性能并不完全相同，但是同样，由于晶粒的多而微小，可认为固体内部是均匀分布着这些晶粒的，其力学性能是各晶粒力学性能的统计平均值。


+ **各向同性假设：无论沿着哪个方向，固体的力学性能都是相同的。** 由众多晶粒构成的金属以及玻璃、塑料等制成的构件，被称作各向同性材料。也有很多各项异性材料，比如木材、胶合板、碳纤维板等纤维增强复合材料。很容易理解的是3d打印工艺制造的构件，从宏观上来说就不具有各向同性，因为沿着z轴的抗拉强度要远低于xy方向。

<center>
<img src="https://raw.githubusercontent.com/Ostoponko/Picstorage/master/img/3%25%5B9C6O%24%24X8P%5B69)0XUU%7EYT.png"
width="40%">
<br>用于拉伸试验的杆件
</center>


## 杆件及基本变形

&emsp;&emsp;材料力学研究的基本构件为**杆件**（长度>>横截面尺寸），此外还有**平板和壳体**。针对杆件的研究已经足以让我们理解构件的力学特性。杆件的四种基本变形的形式是：

<center>

**拉压、剪切、扭转、弯曲**
</center>

对于拉伸压缩、扭转和弯曲，从字面意思上较好理解。剪切是什么意思呢？好比有一个剪刀，将工件从中间剪开，两部分发生错位。
<center>
<img src="https://raw.githubusercontent.com/Ostoponko/Picstorage/master/jianqie.png"
width="25%">
<br>螺栓的剪切变形
</center>


&emsp;&emsp;一个工况复杂的零件可能同时发生几种形变，比如车床的主轴会发生弯曲、扭转、压缩组合变形。

<center>
<img src="https://raw.githubusercontent.com/Ostoponko/Picstorage/master/chexue.png"
width="30%">
<br>工作中的车床
</center>

# 应力和应变

&emsp;&emsp;材料力学研究的物体特性在此之前已经提及，为了研究强度与刚度，我们就要研究应力和应变。这两个概念将要贯穿始终：

+ **应力(Stress)**：物体内的内力**分布**，N/m^2(Pa)
+ **应变(Strain)**：物体内发生的变形，无量纲，%


<center>
<img src="https://raw.githubusercontent.com/Ostoponko/Picstorage/master/F5AEC717BCC9915A23C5B59DA2C012A5.png"
width="30%">
<br>弯曲形变时截面上的应力分布
</center>

&emsp;&emsp;计算应力可以让我们预测构件在什么时候会发生破坏，从而对现有结构进行校核以及改进。想要理解应力，就要先理解内力，因为应力是内力在截面上的分布。在下一章的拉压内容当中，我们会使用简单的截面法求得杆件的内力分布。

<center>
<img src="https://raw.githubusercontent.com/Ostoponko/Picstorage/master/3291F653222419331209AD7FC16CF4A1.png"
width="30%">
<br>单轴加载时垂直截面上的正应力
</center>




