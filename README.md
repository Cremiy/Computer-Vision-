# [Computer-Graph(计算机图形学）](https://cg.cs.tsinghua.edu.cn/#courses.htm)
simple basic knowledge about Computer vision

### 1、什么是色彩

- 色彩是对不同波长光的能量的感知，不同波长的电磁波对应不同的色彩，对于人眼能感知的光（可见光）其波长范围在380nm到760nm之间

- “光”是由不同波长的电磁波按照某种能量分布混合叠加而成。（例如：“白光”则是由所有可见波长的电磁波以相等的强度混合得到。）

- 谱分布：光在各个可见波长的分量的强度分布函数称为光的谱分布。

- 色彩无法用谱分布来进行表示，因为会出现“多谱同色现象”（即多种不同的谱分布出现相同的颜色）

### 2、RGB色彩空间

在所有用于表示颜色色彩的各种色彩空间中，RGB（红绿蓝）色彩空间在计算机图形学中的使用最为广泛：

- 色彩使用三通道RGB向量（r,g,b）来表示

- 在RGB色彩空间中，有部分的常用操作可以通过对RGB三通道分别处理而进行

- 通常可以将r,g,b分别规整化为[0,1]内的浮点数，当使用8bit进行存储时，r,g,b通道常常取值为[0,255]内的整数

- 色彩被表示为三个基本色彩：红色（R），绿色（G），蓝色（B）的线性组合：C=rR+gG+bB

- 为什么选择红绿蓝作为基本色彩？a.以人类视觉的三刺激理论为基础；b.人眼的视网膜中有三种锥状视觉细胞，分别对红、绿、蓝三种光最为敏感

- RGB色彩空间的缺点：一部分色彩无法表示成R、G、B光波的正线性组合。

- 其他常用的色彩空间：CMY、HSV、CIE XYZ

    - CMY：不同于RGB的另外一组基本色彩。C（Cyan青）、M（Magenta品红）、Y（Yellow黄）:分别是R、G、B的补色，C=1-R，M=1-G，Y=1-B
CMY被称为“减色系统”，白[0,0,0],[1,1,1]为黑，RGB称为“加色系统”，白[1,1,1],黑[0,0,0]。CMY模型主要应用于印刷行业。

    - HSV：真实的RGB彩色图像中，色彩种类过多，定位不同的色彩非常困难，HSV则提供了一个非常直观的方法对色彩进行准确的选择，应用于：图像处理、分形图像、光线跟踪。HSV是圆锥形色彩空间，H（Hue色调，色相），描述了基本属性：红、橙、黄、绿、青、蓝、紫等。S(Saturation(饱和度））也叫纯度，饱和度越低，色彩越白。V（Value of brightness亮度），亮度越低，色彩越黑。HSV比RGB更加用户友好。

    - CIE XYZ：解决了RGB所不能表示的负的颜色空间，CIE XYZ可以表示所有感知色彩。色彩基XYZ是色彩基RGB的线性变换。更多应用于色彩科学的研究，与人类感知系统密切相关。

### 3、图像和像素

- 图像和像素的概念
    - 图像可以看成是一个二维离散函数：f(x,y),函数的定义域有矩阵排列着的许多格子组成，这些格子被定义为像素（pixel），分辨率是长宽的乘积。
    - 函数f的取值则为各个像素的色彩：对于彩色图像可以是RGB或者RGBA；对于灰度图像，f为单值函数。(RGBA其中A是透明度通道[0,1]之间，表示图像的透明度）
    
### 4、三角网格

- 图形学的基本目标是什么？
    - 从虚拟的三维场景即相机的位置信息中，生成出一幅二维图像。
    - 三维场景又以怎样的数据结构来表示？
        - 简单的球体，长方体可以直接用参数描述
        - 对于复杂的模型，则需要使用参数曲线和曲面或者更一般的网格模型来进行描述
        - 网格模型之中，又以三角网格最为常用
    - 三角网格是由一系列欧式空间中的三维顶点以及连接这些顶点的若干三角面片组成，具体包括：
        - 顶点集合 V=（V1，V2,....,Vn）
        - 面片集合 F=（f1，f2,....,fm）
        其中，F的每个面片f1都是有V中的顶点构成的空间三角形：
        f1 = (Va1,Vb1,Vc1), f2 = (Va2,Vb2,Vc2)
        





