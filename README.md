# Computer-Vision-
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

    -- CMY：不同于RGB的另外一组基本色彩。C（Cyan青）、M（Magenta品红）、Y（Yellow黄）:分别是R、G、B的补色，C=1-R，M=1-G，Y=1-B
CMY被称为“减色系统”，白[0,0,0],[1,1,1]为黑，RGB称为“加色系统”，白[1,1,1],黑[0,0,0]。CMY模型主要应用于印刷行业。

    -- HSV：真实的RGB彩色图像中，色彩种类过多，定位不同的色彩非常困难，HSV则提供了一个非常直观的方法对色彩进行准确的选择，应用于：图像处理、分形图像、光线跟踪。HSV是圆锥形色彩空间，H（Hue色调，色相），描述了基本属性：红、橙、黄、绿、青、蓝、紫等。S(Saturation(饱和度））也叫纯度，饱和度越低，色彩越白。V（Value of brightness亮度），亮度越低，色彩越黑。HSV比RGB更加用户友好。

    -- CIE XYZ：解决了RGB所不能表示的负的颜色空间，CIE XYZ可以表示所有感知色彩。色彩基XYZ是色彩基RGB的线性变换。更多应用于色彩科学的研究，与人类感知系统密切相关。

### 3、图像和像素

- 图像





