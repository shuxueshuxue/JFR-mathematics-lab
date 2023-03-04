---
{"dg-publish":true,"permalink":"/personal/theory-of-relativity/"}
---


曹老师的课上讲过，然而我并没有完全听懂，且听了就忘了。今天突然想到，于是动手尝试一下。我这里是用纯线性代数的方式，来建立狭义相对论中的参考系的坐标变换公式，不知道和他讲的是否一致。
时空坐标系
![Pasted image 20221106111038.png](/img/user/Personal/Pasted%20image%2020221106111038.png)
我们仅研究物体在一个方向上的运动，因此时空坐标系是二维的。该坐标系中的一个点可以代表一个物体在特定时刻的所处的位置，也可以代表一个事件在某时某地发生。一条曲线可以代表一个物体在一段时间内的运动轨迹，如图中的直线段 $l$ 就代表了一个静止的物体。直线 c 代表了从原点发出的一束光，斜率为光速 c。参照物的坐标设为 $x=0$ 。

变换的参数：目标惯性系与当前惯性系的速度差 v

首先看最简单的伽利略变换公式
$$B=\begin{pmatrix}
1 & 0\\
-v & 1
\end{pmatrix}$$

$$B \begin{pmatrix} t \\ x \end{pmatrix}=\begin{pmatrix} t \\ x-vt \end{pmatrix}$$
这个变换保持所有点的 t 轴坐标不动，只是改动了 x 轴坐标。它的特征向量是 $\begin{pmatrix} 0 \\ 1 \end{pmatrix}$，并没有任何意义。
但我们会看到洛伦兹变换的特征向量是有明确含义的。

要推导公式，我们从几条假设出发
1. 变换是线性变换
2. 变换具有相对性
3. 光速不变

二维时空的线性变换可以表成二维方阵 A(v)，仅四个量有待确定，于是需要四个方程（限制条件）。

我们可以想出来的，有：
- $\begin{pmatrix} 1 \\ c \end{pmatrix},\begin{pmatrix} -1 \\ c \end{pmatrix}$ 是两个特征向量（光速不变）
- $\begin{pmatrix} 1 \\ v \end{pmatrix}$ 的像落在 $t$ 轴上
- 行列式（特征值之积）为 1

第三个条件来自于相对性。考虑 $A(v)$ 和 $A(-v)$ ，它们是互逆的，并且是相似矩阵（相似矩阵的理解：同一个线性变换“切换视角”之后的效果）。 因此它们的行列式都为 1 或 -1，显然 -1 是我们不想要的（特征值都为正，否则会让某一个方向的光逆行），因此只能为 1。

于是我们可以设 A 为
$$\begin{pmatrix}
1 &-1 \\
c &c 
\end{pmatrix}\begin{pmatrix}
 \lambda& \\
 & \frac{1}{\lambda}
\end{pmatrix}\begin{pmatrix}
1 &-1 \\
c &c
\end{pmatrix}^{-1}=\frac{1}{2}\begin{pmatrix}
\lambda+\frac{1}{\lambda} &\frac{1}{c}(\lambda-\frac{1}{\lambda}) \\
c(\lambda-\frac{1}{\lambda}) & \lambda+\frac{1}{\lambda}
\end{pmatrix}$$
注意这其中没有包含 v 的信息。但它能告诉我们所有的洛伦兹变换都是这个形式，用 $v$ 表示不一定比用 $\lambda$ 表示更简洁。不过我们的目的是用 $v$ 表示，因此我们代入
$$A\begin{pmatrix} 1 \\ v \end{pmatrix}=\begin{pmatrix} ? \\ 0 \end{pmatrix}$$
可以解得
$$\lambda=\sqrt{\frac{c-v}{c+v}},\lambda-\frac{1}{\lambda}=\frac{\lambda^2-1}{\lambda}=\frac{-2v}{\sqrt{c^2-v^2}}=\frac{-2v}{c\sqrt{1-v^2/c^2}},\lambda+\frac{1}{\lambda}=\frac{2}{\sqrt{1-v^2/c^2}}$$
令 $\gamma=\dfrac{1}{\sqrt{1-v^2/c^2}}$ ，
$$A=\gamma\begin{pmatrix}
 1&-\dfrac{v}{c^2} \\
 -v& 1
\end{pmatrix}$$	于是
$$A \begin{pmatrix} t \\ x \end{pmatrix}=\gamma\begin{pmatrix} t-\dfrac{v}{c^2}x \\ x-vt \end{pmatrix}=\begin{pmatrix} \dfrac{t-\dfrac{v}{c^2}x}{\sqrt{1-v^2/c^2}}\\ \dfrac{x-vt}{\sqrt{1-v^2/c^2}}\end{pmatrix}$$
这就是洛伦兹变换公式啦！

#### Observation
- 当 $v\ll c$ ，会发现 $\gamma\approx  1$，$A\approx B$ ，说明低速状态下相对论时空观与牛顿力学时空观相容
- 假设有一时钟以 v 速正向运动（$x=vt$），从地面坐标系换到钟坐标系，$\Delta t\to \sqrt{1-v^2/c^2}\ \Delta t$ ，因此地面坐标系中经过 $\dfrac{1}{\sqrt{1-v^2/c^2}}$ s，钟坐标系才会经过 1 s，使得秒针移动一格。该现象即钟慢效应。
- 假设有一长 $x_0$ 的刻度尺以 $v$ 速正向运动，对于像 $x=vt,x=vt+b$ 这样的两条平行线的 x 轴截距之差 $b$ 经过变换会增大至 $\dfrac{b}{\sqrt{1-v^2/c^2}}$，因此该刻度尺的长度 $x_0$ 对应于地面坐标系中 $\sqrt{1-v^2/c^2}\ x_0$ 的长度，即尺缩效应。

#### 相对论推导勾股定理
在一辆以速度 v 向右方向行进的火车上，有一束光 从 $O$ 点射出，（火车上看）垂直射向对面，而地面上看到的情形如图：
![Pasted image 20221106181243.png](/img/user/Personal/Pasted%20image%2020221106181243.png)
由于火车在垂直方向上没有速度，因此我们可以讨论两个参考系中相同的火车的宽度。由于在火车上观测到光线射达对面所用时间为 $t'=\sqrt{1-v^2/c^2}\ t$ ，因此火车宽度为 $\sqrt{c^2-v^2}\ t$ ，再回到地面上看，三条边长符合勾股定理。由于火车的速度（甚至光速）可以任取，我们就证明了勾股定理对任意直角三角形成立。
这个例子并不是游戏，它暗示洛伦兹变换在**更高维**情形下可以成立。

#### 群论性质
坐标变换既然是“变换”，就应该满足结合律，于是我们自然思考能否刻画出它的群结构。
To be continued ...
