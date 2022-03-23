# 前言

## 牛顿力学的三大特点

1、依赖几何直观：多种约束依靠几何直观提供（用以减少对高等数学工具的依赖）

2、以力为主要分析对象进行矢量分析

3、复杂度高：对于有n个独立坐标，且有k个完整约束的力学系统，共需要3n+k个方程以求得系统状态，且各个方程无固定形式。相比之下，拉格朗日力学仅需3n-k个独立方程即可确定系统的位形，且方程形式固定。

## 阅读须知

1、本书已默认读者已经掌握基本的微积分

2、微积分并不是物理现象的本质，甚至数学也不是物理现象的本质，物理自有其本质

# 物理应试的常用方法

## 微元法

极限思想揭示了变量与常量、无限与有限的对立统一关系，是唯物辩证法的对立统一规律在数学领域中的应用。借助极限思想，人们可以从有限认识无限，从“不变”认识“变”，从“直线构成形”认识“曲线构成形”，从量变去认识质变，从近似认识精确。

### 1、非积分（包括微扰法）

#### 例1

![图片2](http://10.129.3.107:5212/#%E5%9B%BE%E7%89%872.png)

如图，一艘船在水面上被一根轻绳拉着前进，已知绳子的末端速度为$v_0$，绳与船相连的一端与水平面夹角为$\theta$，求船的运动速度。

解：
![图片3](C:\Users\fohn\Documents\通用markdown文档\相关图片\图片3.png)

如图，记上方的绳为$AB$，下方的绳为$AC$

设当前滑轮与船之间的绳长为$l$，即$\vert AB \vert=l$

则$\mathrm{d}t$后滑轮与船之间的绳长为$l-v_0\mathrm{d}t$，即$\vert AC \vert=l-v_0\mathrm{d}t$

因为时间足够短，过$l_2$与船的连接点$C$作$AB$的垂线$CD$交$AB$于$E$

可以认为$CD\perp AB$，$CD\perp AC$

$$\therefore\angle ACD=\angle ACD$$
$$\therefore\vert AC\vert=\vert AD \vert=l-v_0\mathrm{d}t$$
$$\therefore\vert BD\vert=v_0\mathrm{d}t$$
$$\therefore x_{ship}=\displaystyle\frac{v_0\mathrm{d}t}{\cos\theta}$$
$$\therefore v_{ship}=\displaystyle\frac{x_{ship}}{dt}=\displaystyle\frac{v_0}{\cos\theta} $$

注：运动的合成与分解也同样可以解决这题。

​        微扰法多用于处于平衡状态的系统，通过对系统进行一个微微小的扰动以分析系统的平衡状态与运动趋势。微扰在运动系统中通常情况下是一个无穷小的、可以指向任意方向的位移。

#### 例2



![图片4](C:\Users\fohn\Documents\通用markdown文档\相关图片\图片4.png)

如图，真空中有两根电阻不计，相距为$l$的金属导轨，有一根质量为$m$的金属棒与电容为$C$的电容将两根金属导轨连接起来，空间中存在与导轨所在平面方向垂直、磁感应强度为$B$的磁场，当拉力$\vec F$向右拉动金属棒时，求棒速度与时间的关系。

解:$$\vec F+I\cdot \vec l\times\vec B=m\vec a=m\displaystyle\frac{\mathrm{d}\vec v}{\mathrm{d}t}$$

$$I=\displaystyle\frac{\mathrm{d}q}{\mathrm{d}t}=\displaystyle\frac{C\mathrm{d}U}{\mathrm{d}t}=C\vert \vec l\times\vec B\vert\cdot\vert\displaystyle\frac{\mathrm{d}\vec v}{\mathrm{d}t}\vert$$

$$\therefore \vec F+C\vert \vec l\times\vec B\vert\cdot \vec l\times\vec B\vert\displaystyle\frac{\mathrm{d}\vec v}{\mathrm{d}t}\vert=m\displaystyle\frac{\mathrm{d}\vec v}{\mathrm{d}t}$$

取模长，得$\vert \vec F\vert-C\vert\vec l\times\vec B\vert^2\cdot\vert\displaystyle\frac{\mathrm{d}\vec v}{\mathrm{d}t}\vert=m\vert\displaystyle\frac{\mathrm{d}\vec v}{\mathrm{d}t}\vert$

$$\therefore \vert a\vert=\displaystyle\frac{\vert\vec F\vert}{m+C\vert\vec l\times\vec B\vert^2}$$

#### 例3

![图片5](C:\Users\fohn\Documents\通用markdown文档\相关图片\图片5.png)

如图，空间中有一被固定住的带正电的小球$A$，有另一可移动的带正电的小球$B$被拴在绳子上，绳子通过$B4$正上方的滑轮。当缓慢拉动绳子末端时，求小球的运动轨迹。

解：缓慢拉绳，系统可近似为处于平衡状态

对当前状态球$B$的进行微扰：

当位移$\delta x$平行于$AB$小球球心的连线时，或者有平行于$AB$小球球心连线的分量时，不难发现系统不能够保持平衡状态。

当位移$\delta x$垂直于$AB$小球球心连线时，可以发现系统仍然能够保持平衡。

记$A$球的球心为$A'$，$B$球的球心为$B'$，

 以，$A’$的运动轨迹为：先在以$B'$为圆心、以$\vert A'B'\vert$为半径的圆上运动，当$A'$到$B'$正上方后，$A'$开始向正上方运动。 

### 2、积分

#### 例4

![图片1](C:\Users\fohn\Documents\通用markdown文档\相关图片\图片1.png)

如图，真空中有两根电阻不计，相距为$l$的金属导轨，有一根质量为$m$，电阻为$r$的金属棒与电阻为$R$的电阻将两根金属导轨连接起来，空间中存在与导轨所在平面方向垂直、磁感应强度为$B$的磁场，当金属棒以$v_0$的初速度运动时，求通过电阻的电量与金属棒速度（大小）的关系（假设金属棒与电阻不相碰且金属棒一直在电阻左侧）。

解：$$I(t)\cdot \vec l\times \vec B=m\displaystyle\frac{\mathrm{d}\vec v}{\mathrm{d}t}$$

$$\therefore I(t)\cdot \mathrm{d}t\cdot\vec l\times \vec B=m\mathrm{d}\vec v$$

$$\therefore \displaystyle\int [I(t)\cdot\vec l\times \vec B]\mathrm{d}t=\displaystyle\int m\mathrm{d}\vec v+\vec C$$

$$\therefore\vec l \times \vec B\cdot\displaystyle=\int I(t)\mathrm{d}t=m\vec v+\vec C$$

$$\therefore q\cdot\vec l\times \vec B=m\vec v+C$$

当t=0时，$I(t)=I(0)=\displaystyle\frac{Blv_0}{R+r},q=\displaystyle\int^0_0I(t)\mathrm{d}t=0,\vec v=\vec v_0$

$$\therefore \vec C=-m\vec v_0$$

$$\therefore q\cdot\vec l\times \vec B=m(\vec v-\vec v_0)$$

取模长，得$Blq=mv-mv_0$

## 对称性分析

自从文明伊始，对称性的概念就以某种形式存在于整个人类社会的语言中了 ——杨振宁

### 1、空间对称性分析

常用于在空间结构上对称的结构，如对称性较强的无穷电阻网络分析

### 2、时间对称性分析

#### 1、时间反演不变性

总有一些物理过程，它们总是以镜像的关系出现在同一个更大的物理过程中。

#### 例5

![图片6](C:\Users\fohn\Documents\通用markdown文档\相关图片\图片6.png)

如图，整个系统无摩擦，当小球从A处释放，是否能到达C点？

解：可以将小球的运动分为两段：A到B，与B到D（D点为小球从B到C运动时所能达到的最高点）

很明显，小球从A到B的运动与从B到D的运动时遵循时间反演不变性的，即小球从B到A的过程与小球从B到D的过程唯一不同的仅是空间上的对称关系，很明显，C点与D点重合，所以小球能够到达C点。

#### 2、对物理过程进行时间反演以化简分析运算过程

已知$AB$在同一条直线上，小滑块以某一速度经过$A$点后以$a$的加速度减速，经过$t$后恰好在$B$点停下，求$AB$间的距离。

解：显然，$x_{AB}=\displaystyle\frac{1}{2}at^2$

##### 例6

![图片12](C:\Users\fohn\Documents\通用markdown文档\相关图片\图片12.png)

已知a、b光以不同的角度射入半圆形玻璃砖内部，在进入玻璃转内部后只剩下一条，判断a光与b光的折射率大小。

对整个系统进行时间反演，则由一道复色光从玻璃砖内射出，被分为a光和b光，很明显，b光的折射率更大。

### 3、关于物理定律的对称性分析

#### 例7

![图片7](C:\Users\fohn\Documents\通用markdown文档\相关图片\图片7.png)

如图，图中蓝色的圆柱为金属圆柱，当闭合开关后，两个金属线圈将会如何运动？

看似这题需要两次分析，但实际上只需要一次：根据楞次定律，线圈必然向磁通量减少的地方运动，因此会远离电路。

#### 例8

$F_洛=q\cdot\vec v\times\vec B$，即洛伦兹力方向指向带电粒子运动所产生的等效电流所受的安培力方向

## 物理概念的贯通

### 1、量纲分析。

通过对量纲的分析判断计算过程是否有误。

### 2、给予图像对物理概念进行分析（本质上仍然是量纲分析）

图像中的每一个运算都有数学意义，但不一定有物理意义。

![图片8](C:\Users\fohn\Documents\通用markdown文档\相关图片\图片8.png)

在图中，两条切线的斜率物理意义就是在该时刻加速度的大小，斜率的正负表示加速度与速度的方向是否同向

在图中，由$(t_1,v_1)$与$(t_2,v_2)$围成的曲边梯形的面积即该物体从$t_1$时刻到$t_2$时刻经过的位移

![图片9](C:\Users\fohn\Documents\通用markdown文档\相关图片\图片9.png)

如图，$S_1=\displaystyle\int_0^{x_0}F(x)\mathrm{d}x=W_F,S_2=\displaystyle\int_0^{t_0}F(t)\mathrm{d}t=I_F$。

但是有一点需要强调，$F$并不是一个二元函数，因为$x$与$t$之间本身就存在一定关系。

![图片10](C:\Users\fohn\Documents\通用markdown文档\相关图片\图片10.png)

$q\displaystyle\frac{\mathrm{d}\varphi}{\mathrm{d}x}=\displaystyle\frac{\mathrm{d}E_p}{\mathrm{d}x}=\mathscr{E}$

![图片11](C:\Users\fohn\Documents\通用markdown文档\相关图片\图片11.png)

$R=\displaystyle\frac{U}{I}\neq\displaystyle\frac{\mathrm{d}U}{\mathrm{d}I}$

## 物理过程的耦合

1、对本质与表达是相同的过程进行合并，用同一表达式进行表达。

2、对在时间上连续、对应不同等效模型的物理过程进行耦合。

## 受力分析

受力分析是牛顿力学中非常重要的一环，经总结受力分析主要有两种方法。

1、先分析主动力，后分析约束力。

定义：主动力是与系统所处状态无关的力，比如万有引力、电场力、安培力和洛伦兹力

定义：约束作用于非自由质点系的力称为约束力，通常情况下未知，需要通过主动力进行求解，比如绳子的弹力、杆的弹力

2、正交分解/力的矢量三角形分解/力的矢量和

## 等效替代法/黑箱方法

戴维南定理：任何一个线性含源二端网络$N$，就其两个端钮$a$、$b$来看，总可以用一个电压源、串联电阻支路来代替。电压源的电压等于该网络$N$的开路电压$U_0$，其串联电阻$R_0$等于该网络中所有独立源为零值时（恒压源短路，恒流源开路）所得网络$N_0$得等效电阻$R_{ab}$。

诺顿定理：含独立源的线性电阻单口网络$N$，就端口特性而言，可以等效为一个电流源和电阻的并联。电流源的电流等于单口网络从外部短路时的端口电流$I$；电阻$R_0$是单口网络内全部独立源为零值时所得网络$N_0$的等效电阻。

![图片13](C:\Users\fohn\Documents\通用markdown文档\相关图片\图片13.png)

在该图中，如果小球的在圆弧上的运动角度足够小（一般小于$\displaystyle\frac{\pi}{36}rad$），则可以将其等效为单摆。

# 公式推导

## 点电荷电势

记无穷远处电势为0

$$\varphi=\displaystyle\frac{E_P}{q}=\displaystyle\frac{1}{q}\displaystyle\int_{+\infty}^{x_0}k\displaystyle\frac{Qq}{r^2}\mathrm{d}r=\displaystyle\frac{1}{q}(k\displaystyle\frac{Qq}{x_0}-0)=k\displaystyle\frac{Q}{x_0}$$

引力势能以及引力势推导公式同理

## 圆周运动加速度

在$\mathrm{d}t$利用弧微分，以弦代替弧，可得

定义$\hat{r}$为与位移同向的单位向量，$\hat{\theta}$为与$\hat{r}$垂直的单位向量，指向曲线轨迹的内侧/曲率圆圆心

显然有$\displaystyle\frac{\mathrm{d}\hat{r}}{\mathrm{d}t}=\displaystyle\frac{\mathrm{d}\theta}{\mathrm{d}t}\hat\theta,\displaystyle\frac{\mathrm{d}\hat\theta}{\mathrm{d}t}=-\displaystyle\frac{\mathrm{d}\theta}{\mathrm{d}t}\hat r$

$$\vec v=\displaystyle\frac{\mathrm{d}\vec r}{\mathrm{d}t}=\displaystyle\frac{\mathrm{d}(r\cdot\hat r)}{\mathrm{d}t}=\displaystyle\frac{\mathrm{d}r}{\mathrm{d}t}\hat r+\displaystyle\frac{\mathrm{d}\hat r}{\mathrm{d}t}r=\displaystyle\frac{\mathrm{d}r}{\mathrm{d}t}\hat r+r\displaystyle\frac{\mathrm{d}\theta}{\mathrm{d}t}\hat\theta$$

$$\vec a=\displaystyle\frac{\mathrm{d}\vec v}{\mathrm{d}t}=[\displaystyle\frac{\mathrm{d}^2r}{\mathrm{d}t^2}-r(\displaystyle\frac{\mathrm{d}\theta}{\mathrm{d}t})^2]\hat r+[r\displaystyle\frac{\mathrm{d}^2\theta}{\mathrm{d}t^2}+2\displaystyle\frac{\mathrm{d}r}{\mathrm{d}t}\cdot\displaystyle\frac{\mathrm{d}\theta}{\mathrm{d}t}]\hat\theta$$

很明显，加速度一共由四项构成，第一项为$r$变化引起的加速度，第二项为向心加速度，第三项为角加速度引起的加速度，第四项为科里奥利加速度

当物体仅做匀速圆周运动时，$\vec a=r(\displaystyle\frac{\mathrm{d}\theta}{\mathrm{d}t})^2\hat r$

取模长，得$a=(\displaystyle\frac{\mathrm{d}\theta}{\mathrm{d}t})^2r=\omega^2r$

## $n$匝面积为S的线圈以$\omega$的角速度在磁感应强度为$B$的磁场中转动

$\mathscr{E}=\displaystyle\frac{\mathrm{d}\Phi}{\mathrm{d}t}=nBS\displaystyle\frac{\mathrm{d}\sin(\omega t+\varphi)}{\mathrm{d}t}=nBS\omega\cos(\omega t+\varphi)$

## 正弦交流电的有效值

$$Q=\displaystyle\int^t_0I^2r\mathrm{d}t=\displaystyle\int^t_0\displaystyle\frac{U^2}{r}\mathrm{d}t=\displaystyle\int^t_0\displaystyle\frac{[nBS\omega\cos(\omega t+\varphi)]^2}{r}\mathrm{d}t=\displaystyle\frac{(nBS\omega)^2}{2r}\displaystyle\int^t_0\vert\cos(2\omega t+2\varphi)-1\vert\mathrm{d}t$$

当$t=k\displaystyle\frac{2\pi}{\omega},k\in\mathbb{N}^+$时，$Q=\displaystyle\frac{(nBS\omega)^2}{2r}t$

$$\therefore \displaystyle\frac{(nBS\omega)^2}{2r}t=I^2rt$$

$I=\displaystyle\frac{nBS\omega}{\sqrt{2}r}=\displaystyle\frac{I_{max}}{\sqrt{2}}$

## 公式5

![图片14](C:\Users\fohn\Documents\通用markdown文档\相关图片\图片14.png)

如图，真空中有两根电阻不计，相距为$l$的金属导轨，有一根质量为$m$，电阻为$r$的金属棒与电动势为$E$，内阻忽略不计电源的将两根金属导轨连接起来，空间中存在与导轨所在平面方向垂直、磁感应强度为$B$的磁场，记金属棒以水平初速度$v_0$地放到金属导轨上的时刻为0时刻，求金属棒的速度（大小）关于时间的表达式。

解：$$B\displaystyle\frac{E-Blv}{r}l=m\displaystyle\frac{\mathrm{d}v}{\mathrm{d}t}$$

$$\therefore \displaystyle\frac{\mathrm{d}t}{m}=\displaystyle\frac{\mathrm{d}v}{\displaystyle\frac{BEl}{r}-\displaystyle\frac{B^2l^2}{r}v}$$

$$\therefore \displaystyle\frac{t}{m}=-\displaystyle\frac{r}{B^2l^2}[\ln(\displaystyle\frac{BEl}{r}-\displaystyle\frac{B^2l^2}{R}v)-\ln(\displaystyle\frac{BEl}{r}-\displaystyle\frac{B^2l^2}{r}v_0)]$$

$$\therefore E-Blv=\displaystyle\frac{E-Blv_0}{e^{\frac{B^2l^2}{rm}t}}$$

$$\therefore v=\displaystyle\frac{1}{Bl}(E-\displaystyle\frac{E-Blv_0}{e^{\frac{B^2l^2}{rm}t}})<\displaystyle\frac{E}{Bl}$$

## 简谐运动方程

### 无阻尼自由震动

$$F=-kx$$

$$\therefore m\displaystyle\frac{\mathrm{d}^2x}{\mathrm{d}t^2}+kx=0$$

$\therefore$其特征方程为$$r^2+\omega^2=0$$

$$\therefore r_{1,2}=\pm i\omega$$

$\therefore$通解为$$x=C_1\sin\omega t+C_2\cos\omega t=\sqrt{C_1^2+C_2^2}(\displaystyle\frac{C_1}{\sqrt{C_1^2+C_2^2}}\sin\omega t+\displaystyle\frac{C_2}{\sqrt{C_1^2+C_2^2}}\cos\omega t)=A\sin(\omega t+\varphi)$$

### 无阻尼强迫震动

设外力为$f(x)=f_0\sin pt$

$$\therefore m\displaystyle\frac{\mathrm{d}^2x}{\mathrm{d}t^2}+kx=h\sin pt,h=\displaystyle\frac{f_0}{m}$$

当$p\neq \omega$时，通解为$$x=\displaystyle\frac{h}{\omega^2-p^2}\sin pt+C_1\sin\omega t+C_2\cos\omega t=\displaystyle\frac{h}{\omega^2-p^2}\sin pt+A\sin(\omega t+\varphi)$$

当$p=\omega$时，$$x=-\displaystyle\frac{h}{2\omega}t\cos pt+A\sin(\omega t+\varphi)$$

显然当$p=\omega$时，函数$x(t)$无界，也解释了为什么共振会有这么大的威力。

### LC振荡回路

电容器极板上的电荷量为$q$， 电路中的电流为$i$，并取LC回路的顺时针方向为电流的正方向。线圈两端的电势差应和电容器两极板之间的电势差相等，即$$-L\displaystyle\frac{\mathrm{d}i}{\mathrm{d}t}=\displaystyle\frac{q}{C}$$

根据电流的定义式$i=\displaystyle\frac{\mathrm{d}q}{\mathrm{d}t}$，有$$\displaystyle\frac{\mathrm{d}^2q}{\mathrm{d}t^2}=-\displaystyle\frac{1}{LC}q$$

$$\therefore q=Q_0\cos(\omega t+\varphi),\omega^2=\displaystyle\frac{1}{LC}$$

$$i=\displaystyle\frac{\mathrm{d}q}{\mathrm{d}t}=-\omega Q_0\cos(\omega t+\varphi)$$

考虑回路中的能量：

$$W_e=\displaystyle\frac{q^2}{C}=\displaystyle\frac{Q_0^2}{C}\cos^2(\omega t+\varphi)$$

$$W_m=\displaystyle\frac{1}{2}Li^2=\displaystyle\frac{L\omega^2Q_0^2}{2}\sin(\omega t+\varphi)$$

很显然在LC振荡回路的无阻尼自由振动中，能量在电场能与磁场能之间转换，但是总体能量保持不变。

## 平面简谐波动方程

假设原点的振动方程为$y=A\sin(\omega t+\varphi)$，设P点距离原点$x$

$$\therefore y_P=A\cos[\omega(t-\displaystyle\frac{x}{v})+\varphi]=A\cos[\omega t-\displaystyle\frac{2n}{\lambda}x+\varphi]$$

## 动能定理证明

$$\vec F\mathrm{d}t=m\mathrm{d}\vec v$$

$$\vec F\cdot \vec v\mathrm{d}t=m\cdot\vec v\mathrm{d}\vec v$$

$$\vec F\cdot\vec v\mathrm{d}t=\mathrm{d}(\displaystyle\frac{1}{2}m\vec v^2)$$

$$\vec F\cdot\vec v=\displaystyle\frac{1}{2}m\vec v^2_2-\displaystyle\frac{1}{2}m\vec v^2_1$$

## 动量定理证明

$$\vec F\mathrm{d}t=m\mathrm{d}\vec v$$

$$\vec F\mathrm{d}t=\mathrm{d}m\vec v$$

$$F\cdot t=m\vec v_2-m \vec v_1$$

## 相对论中能量、动量的关系

相对性原理（狭义）：物理定律在一切惯性系中形式不变

光速不变原理（狭义）：光在一切惯性系内传播速度不变

设参考系$K(O-xyz)$与$K'(O'-x'y'z')$均为惯性系

若$x/\mskip-4mu/ x',y/\mskip-4mu/ y',z/\mskip-4mu/ z'$，$K'(O'-x'y'z')$以$v_x=v,v_y=0,v_z=0$的速度相对于$K(O-xyz)$运动，可以得到如下坐标变换公式：
$$
\left\{
\begin{aligned}
&x'=\displaystyle\frac{x-vt}{\sqrt{1-\displaystyle\frac{v^2}{c^2}}}\\
&y'=y\\
&z'=z\\
&t'=\displaystyle\frac{t-\displaystyle\frac{vx}{c^2}}{\sqrt{1-\displaystyle\frac{v^2}{c^2}}}
\end{aligned}
\right.
\left\{
\begin{aligned}
&x=\displaystyle\frac{x'+vt}{\sqrt{1-\displaystyle\frac{v^2}{c^2}}}\\
&y'=y\\&z'=z\\
&t=\displaystyle\frac{t'+\displaystyle\frac{v_x}{c^2}}{\sqrt{1-\displaystyle\frac{v^2}{c^2}}}
\end{aligned}
\right.
$$



在$K$系中，$$u_x=\displaystyle\frac{\mathrm{d}x}{\mathrm{d}t},u_y=\displaystyle\frac{\mathrm{d}y}{\mathrm{d}t},u_z=\displaystyle\frac{\mathrm{d}x}{\mathrm{d}t}$$

同理，$$K':u_x'=\displaystyle\frac{\mathrm{d}x'}{\mathrm{d}t'},u_y'=\displaystyle\frac{\mathrm{d}y'}{\mathrm{d}t'},u_z'=\displaystyle\frac{\mathrm{d}x'}{\mathrm{d}t'}$$

因此有如下变换公式：
$$
\left\{
\begin{aligned}
&u_{x'}=\displaystyle\frac{u_x-v}{1-\displaystyle\frac{v}{c^2}u_x}\\
&u_{y'}=\displaystyle\frac{u_y\sqrt{1-\beta^2}}{1-\displaystyle\frac{u}{c^2}u_x}\\
&u_{z'}=\displaystyle\frac{u_z\sqrt{1-\beta^2}}{1-\displaystyle\frac{u}{c^2}u_x}\\
\end{aligned}
\right.
\left\{
\begin{aligned}
&u_{x}=\displaystyle\frac{u_{x'}+v}{1-\displaystyle\frac{v}{c^2}u_{x'}}\\
&u_{y}=\displaystyle\frac{u_{y'}\sqrt{1-\beta^2}}{1-\displaystyle\frac{u}{c^2}u_{x'}}\\
&u_{z}=\displaystyle\frac{u_{z'}\sqrt{1-\beta^2}}{1-\displaystyle\frac{u}{c^2}u_{z'}}\\
\end{aligned}
\right.
$$
以及由此可以得出一系列结论：

在$K$系中的观察者观察到$A(x_1,y_1,z_1,t_1)$与$B(x_2,y_2,z_2,t_2)$同时发生，在$K'$系中的观察者会观察到$\Delta t=\displaystyle\frac{\displaystyle\frac{v}{c^2}(x_1-x_2)}{\sqrt{1-\beta^2}}$。

同理，以$K$为参考系，经过时间为$t_0$，则在$K'$系中经过的时间为$\displaystyle\frac{t_0}{\sqrt{1-\beta^2}}$（钟慢效应），以$K$为参考系，长为$l$的杆在$K'$中沿着$x'$轴运动，观察者会认为其长度为$l'$，则$l=\displaystyle\frac{l'}{\sqrt{1-\beta^2}}$（尺缩效应）

在狭义相对论中，$m=\displaystyle\frac{m_0}{\sqrt{1-\beta^2}}$，$m_0$为静质量， $p=\displaystyle\frac{m_0}{\sqrt{1-\beta^2}}v$，$\therefore F=\displaystyle\frac{\mathrm{d}p}{\mathrm{d}t}$

定义$v=\displaystyle\frac{\mathrm{d}E_k}{\mathrm{d}p}$

$\therefore \mathrm{d}E_k=v\mathrm{d}mv=v^2\mathrm{d}m+mv\mathrm{d}v$，将质量变换公式代入，得$m^2(c^2-v^2)=m_0^2c^2$，微分得$mv\mathrm{d}v=(c^2-v^2)\mathrm{d}m$，$\therefore \mathrm{d}E_k=c^2\mathrm{d}m$，这说明当质点的速度增大时，$m$与$E_k$都增加。积分得，$\displaystyle\int_0^{E_k}\mathrm{d}E_k=\displaystyle\int_{m_0}^mc^2\mathrm{d}m$，$\therefore E_k=m_0c^2(\displaystyle\frac{1}{\sqrt{1-\frac{v^2}{c^2}}}-1)$，泰勒展开，得$E_k=\displaystyle\frac{1}{2}m_0v^2+\displaystyle\frac{3}{8}m_0\displaystyle\frac{v^4}{c^2}+\cdots$，当$v$比较小时，$E_k=\displaystyle\frac{1}{2}m_0v^2$

$\because v=\displaystyle\frac{\mathrm{d}E_k}{\mathrm{d}p}，\therefore\mathrm{d}E_k=v\mathrm{d}p$，考虑$m$不变时，即$E_k=\displaystyle\int_0^p\displaystyle\frac{p}{m}\mathrm{d}p=\displaystyle\frac{p^2}{2m}$；当考虑$m$变化时，即$E=mc^2$与$\mathrm{d}E_k=c^2\mathrm{d}m$相乘，并考虑$\mathrm{d}E=\mathrm{d}E_k$，得$E\mathrm{d}E=mc^2v\mathrm{d}p=c^2p\mathrm{d}p$，积分得$\displaystyle\frac{1}{2}(E^2-E_0^2)=\displaystyle\int_{E_0}^{E}E\mathrm{d}E=\displaystyle\int_0^pc^2p\mathrm{d}p=\displaystyle\frac{1}{2}c^2p^2$，得$E^2=c^2p^2+m_0^2c^4$

## 安培力做负功等于电能的增加量的证明

不妨取系统中只有安培力做负功

$\therefore$有$-W_安=\displaystyle\frac{1}{2}mv^2-\displaystyle\frac{1}{2}mv_0^2$

即证$\displaystyle\int_0^tE\mathrm{d}q=\displaystyle\frac{1}{2}mv_t^2-\displaystyle\frac{1}{2}mv_0^2$

$$BIl=m\displaystyle\frac{\mathrm{d}v}{\mathrm{d}t}$$

$$BIl\mathrm{d}t=m\mathrm{d}v$$

积分，得 $$Bql=mv_t-mv_0$$

$$\therefore \displaystyle\int_0^tE\mathrm{d}q=\displaystyle\int_{v_0}^{v_t}Blv\mathrm{d}\displaystyle\frac{mv-mv_0}{Bl}$$

令$x=\displaystyle\frac{mv-mv_0}{Bl}$，$$\therefore E_电=\displaystyle\frac{B^2l^2}{m}\displaystyle\int_0^{x_t}x\mathrm{d}x+Bl\displaystyle\int_0^{x_t}v_0\mathrm{d}x=\displaystyle\frac{1}{2}\displaystyle\frac{B^2l^2}{m}\displaystyle\frac{m^2(v_t-v_0)^2}{B^2l^2}+Blv_0\cdot\displaystyle\frac{mv_t-mv_0}{Bl}=\displaystyle\frac{1}{2}mv_t^2-\displaystyle\frac{1}{2}mv_0^2$$

事实上，其他力的做功与冲量也必须在考虑范围之内，这里的证明是最简单的形式的证明。

## 柯尼希定理证明完全非弹性碰撞损失能量最多

以两个物体为例

碰撞发生前，物体$A,B$的相对质心速度分别为$\vec v_1,\vec v_2$,$A,B$质量分别为$m_1,m_2$

$\therefore m_1\vec v_1+m_2\vec v_2=m_1\vec v_1'+m_2\vec v_2'$

当$\vec v_1'=\vec v_2'=\vec0$时，即发生完全非弹性碰撞

$\Delta E_k=\displaystyle\frac{1}{2}m\vec v_1^2+\displaystyle\frac{1}{2}m\vec v_2^2\geq \displaystyle\frac{1}{2}m\vec v_1^2+\displaystyle\frac{1}{2}m\vec v_2^2-\displaystyle\frac{1}{2}m\vec v_1'^2-\displaystyle\frac{1}{2}m\vec v_2'^2$

在碰撞前后，质心的速度保持不变，为$\displaystyle\frac{m_1\vec v_1+m_2\vec v_2}{m_1+m_2}$，显然质心动能保持不变

故完全非弹性碰撞损失能量最多

## 单摆周期求解

在单摆摆动过程中显然有$$\displaystyle\frac{1}{2}mv^2+mgl(1-\cos\theta)=const$$

令$\alpha$为最大摆角

$$\displaystyle\frac{1}{2}mv^2+mgl(1-\cos\theta)=mgl(1-\cos\alpha)$$

$$\therefore \displaystyle\frac{1}{2}mv^2=mgl(\cos\theta-\cos\alpha)$$

$$v=\displaystyle\frac{\mathrm{d}l\theta}{\mathrm{d}t}=l\displaystyle\frac{\mathrm{d}\theta}{\mathrm{d}t}$$

$$\therefore (\displaystyle\frac{\mathrm{d}\theta}{\mathrm{d}t})^2=\displaystyle\frac{2g}{l}(\cos\theta-\cos\alpha)$$

$$\displaystyle\frac{\mathrm{d}\theta}{\mathrm{d}t}=2\sqrt{\displaystyle\frac{2g}{l}}(\sin^2\displaystyle\frac{\alpha}{2}-\sin^2\displaystyle\frac{\theta}{2})^\frac{1}{2}$$

$$\therefore t=\displaystyle\frac{1}{2}\sqrt{\displaystyle\frac{l}{g}}\displaystyle\int_0^\theta\displaystyle\frac{\mathrm{d}\theta}{\sqrt{\sin^2\displaystyle\frac{\alpha}{2}-\sin^2\displaystyle\frac{\theta}{2}}}$$

若有$\sin\displaystyle\frac{\theta}{2}=\sin\displaystyle\frac{\alpha}{2}\cdot\sin\displaystyle\frac{\varphi}{2}$

$$\therefore \displaystyle\frac{1}{2}\cos\displaystyle\frac{\theta}{2}\mathrm{d}\theta=\sin\displaystyle\frac{\alpha}{2}\cos\varphi\mathrm{d}\varphi$$

$$\therefore t=\sqrt{\displaystyle\frac{l}{g}}\displaystyle\int_0^\varphi\displaystyle\frac{\mathrm{d}\varphi}{\sqrt{1-\sin^2\displaystyle\frac{\alpha}{2}\sin^2\varphi}}$$

$$\therefore T=4\sqrt{\displaystyle\frac{l}{g}}\displaystyle\int_0^\frac{\pi}{2}\displaystyle\frac{\mathrm{d}\varphi}{\sqrt{1-\sin^2\displaystyle\frac{\alpha}{2}\sin^2\varphi}}$$

当$\alpha$小于$\displaystyle\frac{\pi}{36}rad$时，$\displaystyle\int_0^\frac{\pi}{2}\displaystyle\frac{\mathrm{d}\varphi}{\sqrt{1-\sin^2\displaystyle\frac{\alpha}{2}\sin^2\varphi}}\approx\displaystyle\frac{\pi}{2}$

## 机车恒功率启动速度关于时间的表达式

$$\displaystyle\frac{p}{v}-f=m\displaystyle\frac{\mathrm{d}v}{\mathrm{d}t}$$

$$\therefore \displaystyle\frac{\mathrm{d}t}{m}=\displaystyle\frac{v\mathrm{d}v}{p-fv}$$

$$\therefore -\displaystyle\frac{\mathrm{d}t}{m}=(\displaystyle\frac{1}{f}+\displaystyle\frac{1}{\displaystyle\frac{f^2}{p}v-f})\mathrm{d}v$$

积分，得$$-\displaystyle\frac{t}{m}+C=\displaystyle\frac{v}{f}+\displaystyle\frac{p}{f^2}\ln(f-\displaystyle\frac{f^2}{p}v)$$

当$t\rightarrow0$时，$v\rightarrow0$，$\therefore C=\displaystyle\frac{p}{f^2}\ln f$

令$1-\displaystyle\frac{f}{p}v=x$

$$\therefore -\displaystyle\frac{t}{m}=\displaystyle\frac{p}{f^2}(1-x)+\displaystyle\frac{p}{f^2}\ln x$$

$$\therefore x-\ln x=1+\displaystyle\frac{f^2}{pm}t$$

$$\therefore \displaystyle\frac{e^x}{x}=e^{1+\displaystyle\frac{f^2}{pm}t}$$

考虑$F(x)$为$f(x)=\displaystyle\frac{e^x}{x}$在$x\in (0,1]$上的反函数

$$\therefore x=F(e^{1+\displaystyle\frac{f^2}{pm}t})$$

$$\therefore v=\displaystyle\frac{p}{f}-\displaystyle\frac{p}{f}e^{1+\displaystyle\frac{f^2}{pm}t}$$

当$t\rightarrow +\infty$时，$v\rightarrow \displaystyle\frac{p}{f}$

注：$$f(x)=\displaystyle\frac{e^x}{x},f'(x)=\displaystyle\frac{e^x(x-1)}{x^2}$$
 
在$x\in(0,1]$上有$f(x)\downarrow$恒成立

$\therefore f(x)$在$x\in (0,1]$上有反函数$F(x),x\in[e,+\infty),F(x)\in(0,1]$

$F(x)=\displaystyle\int_0^x\displaystyle\frac{1}{f'(x)}\mathrm{d}x=\displaystyle\int_0^x\displaystyle\frac{x^2}{e^x(x-1)}\mathrm{d}x$

## 万有引力定律推导
引理：Binet公式
$$\vec a=\displaystyle\frac{\mathrm{d}\vec v}{\mathrm{d}t}=[\displaystyle\frac{\mathrm{d}^2r}{\mathrm{d}t^2}-r(\displaystyle\frac{\mathrm{d}\theta}{\mathrm{d}t})^2]\hat r+[r\displaystyle\frac{\mathrm{d}^2\theta}{\mathrm{d}t^2}+2\displaystyle\frac{\mathrm{d}r}{\mathrm{d}t}\cdot\displaystyle\frac{\mathrm{d}\theta}{\mathrm{d}t}]\hat\theta=[\ddot r-r(\dot\theta)^2]\hat{r}+[r\ddot\theta+2\dot r\dot\theta]\hat\theta$$
$$\left\{
\begin{aligned}
\vec a&=[\ddot r-r(\dot\theta)^2]\hat{r}+[r\ddot\theta+2\dot r\dot\theta]\hat\theta\\
\vec F&=F\cdot \hat r
\end{aligned}
\right.$$
$$\therefore 
\left\{
\begin{aligned}
\displaystyle\frac{F}{m}=\ddot r-r(\dot\theta)^2\\
2\dot r\dot\theta+r\ddot\theta=0
\end{aligned}
\right.$$
$$\because 2\dot r\dot\theta+r\ddot\theta=0$$
$$\therefore \int (2r\dot r\dot\theta+r^2\ddot\theta)\mathrm{d}t=r^2\dot\theta+C$$
$$\text{令}r^2\dot\theta=h$$
$$\therefore \dot\theta=\displaystyle\frac{h}{r^2}$$
$$\text{令}u=\displaystyle\frac{1}{r}$$
$$\displaystyle\frac{\mathrm{d}r}{\mathrm{d}t}=\displaystyle\frac{\mathrm{d}\frac{1}{u}}{\mathrm{d}t}=\displaystyle\frac{\mathrm{d}\frac{1}{u}}{\mathrm{d}u}\displaystyle\frac{\mathrm{d} u}{\mathrm{d} t}=-\frac{1}{u^2}\cdot\displaystyle\frac{\mathrm{d}u}{\mathrm{d}\theta}\displaystyle\frac{\mathrm{d}\theta}{\mathrm{d}t}=-h\displaystyle\frac{\mathrm{d}u}{\mathrm{d}\theta}$$
$$\displaystyle\frac{\mathrm{d}^2r}{\mathrm{d}t^2}=-h\cdot\displaystyle\frac{\mathrm{d}}{\mathrm{d}\theta}(\displaystyle\frac{\mathrm{d}u}{\mathrm{d}\theta})\displaystyle\frac{\mathrm{d}\theta}{\mathrm{d}t}=-\displaystyle\frac{h^2}{r^2}\displaystyle\frac{\mathrm{d}^2u}{\mathrm{d}\theta^2}$$
$$\therefore -h^2u^2\displaystyle\frac{\mathrm{d}^2u}{\mathrm{d}\theta^2}+u=-\displaystyle\frac{F}{mh^2u^2}$$
$$\\$$

根据开普勒第二定律，有$\dot A=C$

在极坐标条件下，有$\dot A=\displaystyle\frac{r^2\dot\theta}{2}$

根据开普勒第三定律，$$r=\displaystyle\frac{p}{1+e\cos\theta}$$

代入Binet公式可得$$F=-\displaystyle\frac{h^2}{p}\displaystyle\frac{m}{r^2}$$
根据开普勒第三定律，当径矢扫过全部椭圆后，$A=\pi ab$
$$\because 2\dot A=r^2\dot\theta=h$$

积分可得$2\pi ab=hT$
$$\therefore \displaystyle\frac{T^2}{a^3}=\displaystyle\frac{4\pi^2b^2}{h^2a}=\displaystyle\frac{4\pi^2p}{h^2}$$
$$\therefore \displaystyle\frac{h^2}{p}=k^2$$
$$\therefore F=-\displaystyle\frac{mk^2}{r^2}$$
因为力的作用是相互的
$$\therefore F\varpropto m_sm$$
$$\therefore k^2=Gm_s$$
$$F=-\displaystyle\frac{Gm_sm}{r^2}$$