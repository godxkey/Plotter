### 上架一个APP：漫谈开发Plotter的缘由和技术

在学校的课余时间，陆陆续续开发了两个星期，APP终于在应用市场上架了：https://www.coolapk.com/apk/284166

不仅如此，Plotter也已经开源，GItHub链接就放到文末了。

先说Plotter是什么：一个轻量级、跨平台、不依赖网络的便携性科学计算软件。事实上Plotter不是一个游戏，而是一种非常**硬核**，**极少人愿意去做**、或者做的好的软件——数模软件/计算器。

Plotter的特点使得它所面向的用户有：

- 中小学生：带单位的四则运算、简单的函数绘图、组合学运算、统计学运算
- 大学生：向量/矩阵的运算、数值微积分、多元函数的极值等
- 教育工作者：通过图像和更具化的运算方式带给学生更深刻的概念
- 工程师：全平台，无论在哪台设备都能允许，且可以脱机运行
- 程序员：各种进制之间的转换和运算，超高精度浮点数或者大整数的运算
- 科研人员：
  - 便携性使得无论何时何地产生了灵感，立马就可以拿出设备进行计算和实验
  - 带单位的运算使得科研人员能在计算时带单位运算，在任何时候可以进行带单位数值的转换，还使得在计算数据时保证量纲不出错
  - 在任何时候引入高精度带单位的常量进行运算，例如普朗克常数、阿伏伽德罗常数等

**Q:** 教育工作者已经有像Desmos、Geogebra这样的专业软件了，不同的工程师也有各自领域的专业软件，科研工作者更是有像MATLAB、Mathematica、Python这样的专业工具了，那Plotter的意义何在？

**A:** Plotter的意愿是让科学计算变的更加简单和容易。Plotter封装了不同领域都可能用到的功能，使其受众较广泛，其设计使得它能够在任何平台上脱机运行，尤其是移动端，这使得软件的通用性和便携性很强。

**Q:** 让科学计算变的更加简单和容易能带来什么？

**A:** 现代科学技术的突飞猛进离不开计算机的产生。无论是对DNA的测序还是蛋白质结构的模拟，让现代生物学突飞猛进发展到新的阶段，产生了生物信息学。同样对大脑神经元的模拟推进了脑科学的发展，对医药数据的分析带来的科学发现造福了无数疾病中的苦难人群。有限元分析使得我们能够在计算机上模拟物理过程，广泛运用于工业。对天体运行的模拟造就了现在的天文学和航天学。对化学分子运动的模拟而发现了新的催化剂......不知道多少科学家用MATLAB分析实验数据，多少数学家用Mathematica进行符号运算。

因此可以说：新的科学发现是在以人类智慧驱动下的科学计算中产生的。

计算机科学家、粒子物理学家 Stephen Wolfram 曾提到计算本身也是一种新科学，存粹的计算也可能发现宇宙的规律......

Plotter的体量并没有那么大，它仅仅是做到了轻量便携和脱机而已，但它的意愿仍是使得科学计算变的更加简单和容易。

那么下面我就废话不多说啦，分享一下在Plotter开发中所使用到的一些技术~

#### 技术

