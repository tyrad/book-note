## 前言
#### 本书涵盖的数学思想
- 多维空间
	- 你可能对二维(2D)和三维(3D)这两个词的意思有一些直观的了解。我们生活在三维世界里，而二维世界是平面的，就像一张纸或一面计算机屏幕。二维世界中的一个具体位置可以用两个数（通常称为x坐标和y坐标）来描述，而在三维时间中则需要3个数来定位一个位置。我们无法想象一个17维的空间，但是可以用包含17个数的列表来描述其中的点。像这样的数字列表被称为**向量**，向量数学有助于更好的阐述“纬度”这一概念。
- 函数空间
	- 有时，一个数字列表可以指定一个函数。举个例子，有两个数`a=5`和`b=13`，就可以创建一个形式为`f(x)=ax+b`的(线性)函数。在这种情况下，函数就是`f(x)=5x+13`。对于二维空间中的每一个点（表示为坐标`(a,b)`），都有一个线性函数与之对应。所以可以把所有线性函数的集合看作一个二维空间。
- 导数和梯度
	- 测量函数变化率的微积分运算。**导数**可以反映当输入值x变大时，函数`f(x)`增大或减小的速度。在三维空间中，函数肯恩看起来像`f(x,y)`，当改变x或y的值时，它的值会增大或减小。把`(x,y)`对看作二维空间中的点，也许你会问，在这个二维空间中，朝哪个方向走能使`f`增大得最快。梯度给出了答案。
- 函数优化
	- 对于`f(x)`或`f(x,y)`这种形式的函数，有一个更宽泛的问题：函数的哪些输入会产生最大的输出？对于`f(x)`,答案是某个值`x`；而对于`f(x,y)`，答案则是二维空间中的一个点。在二维的情况下，梯度可以帮助我们找到答案。如果梯度告诉我们`f(x,y)`在某个方向上不断增大，那么朝这个方向前进，就可以找到`f(x,y)`的最大值。同样，在寻找一个函数的最小值时，类似的策略也适用。
- 用函数预测数据
	- 假如你想预测某个数据，比如某一时刻的股票价格。可以创建一个函数`p(t)`，其输入为时间`t`，输出价格`p`。衡量函数预测质量的标准是它与实际数据的接近程度，从这个意义上说，寻找预测函数意味着将函数和实际数据之间的误差最小化。要做到这一点，需要探讨一函数的一个空间，并找到一个最小值。这就是所谓的**回归**。