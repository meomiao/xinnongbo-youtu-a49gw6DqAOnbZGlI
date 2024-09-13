[合集 \- manim(35\)](https://github.com)[1\.【manim动画教程】\-\- 安装2023\-03\-28](https://github.com/wang_yb/p/17264724.html)[2\.【manim动画教程】\-\- 基本图形2023\-03\-29](https://github.com/wang_yb/p/17269340.html)[3\.【manim动画教程】\-\- 坐标系2023\-04\-10](https://github.com/wang_yb/p/17301528.html)[4\.【manim动画教程】\-\- 文本样式2023\-04\-07](https://github.com/wang_yb/p/17294918.html)[5\.【manim动画教程】\-\- 文字和公式2023\-04\-04](https://github.com/wang_yb/p/17285467.html)[6\.【manim动画教程】\-\- 图形样式2023\-03\-31](https://github.com/wang_yb/p/17275154.html)[7\.【manim动画教程】\-\-相机2023\-04\-19](https://github.com/wang_yb/p/17334029.html)[8\.【manim动画教程】\-\-高级动画效果2023\-04\-14](https://github.com/wang_yb/p/17317576.html)[9\.【manim动画教程】\-\-常用动画效果2023\-04\-12](https://github.com/wang_yb/p/17309865.html)[10\.【manim】之滚动字幕2022\-12\-06](https://github.com/wang_yb/p/16955924.html)[11\.【manim】之圆规动画2023\-01\-31](https://github.com/wang_yb/p/17079903.html)[12\.【manim】之目录动画2023\-02\-28](https://github.com/wang_yb/p/17163051.html)[13\.manim边学边做\-\-DecimalNumber06\-12](https://github.com/wang_yb/p/18243662)[14\.manim边学边做\-\-Integer06\-13](https://github.com/wang_yb/p/18245670)[15\.manim边学边做\-\-Variable06\-14](https://github.com/wang_yb/p/18248823)[16\.manim边学边做\-\-Title06\-20](https://github.com/wang_yb/p/18258229)[17\.manim边学边做\-\-BulletedList06\-21](https://github.com/wang_yb/p/18261017)[18\.manim边学边做\-\-SingleStringMathTex06\-23](https://github.com/wang_yb/p/18264154):[westworld加速](https://tianchuang88.com)[19\.manim边学边做\-\-MathTex06\-28](https://github.com/wang_yb/p/18272507)[20\.manim边学边做\-\-Tex07\-01](https://github.com/wang_yb/p/18278554)[21\.manim边学边做\-\-Text07\-04](https://github.com/wang_yb/p/18284013)[22\.manim边学边做\-\-Paragraph07\-09](https://github.com/wang_yb/p/18291657)[23\.manim边学边做\-\-MarkupText07\-10](https://github.com/wang_yb/p/18294000)[24\.manim边学边做\-\-Code07\-16](https://github.com/wang_yb/p/18304450)[25\.manim边学边做\-\-Matrix07\-17](https://github.com/wang_yb/p/18307871)[26\.manim边学边做\-\-Table07\-25](https://github.com/wang_yb/p/18322456)[27\.manim边学边做\-\-点08\-09](https://github.com/wang_yb/p/18351279)[28\.manim边学边做\-\-圆形类08\-15](https://github.com/wang_yb/p/18361469)[29\.manim边学边做\-\-圆弧形08\-20](https://github.com/wang_yb/p/18368851)[30\.manim边学边做\-\-直线类08\-22](https://github.com/wang_yb/p/18374417)[31\.manim边学边做\-\-带箭头直线09\-02](https://github.com/wang_yb/p/18392446)[32\.manim边学边做\-\-曲线类09\-04](https://github.com/wang_yb/p/18396028)[33\.manim边学边做\-\-角度标记09\-07](https://github.com/wang_yb/p/18401449)[34\.manim边学边做\-\-常用多边形09\-10](https://github.com/wang_yb/p/18406455)35\.manim边学边做\-\-通用多边形09\-13收起
`manim`提供了**通用多边形**模块，可以绘制任意的多边形。


通用多边形模块有两种，`Polygon`和`Polygram`。


`Polygon`是一个几何学术语，主要指的是由三条或三条以上的线段首尾顺次连接所组成的平面图形，


而`Polygram`的含义更加广泛一些，它除了可以绘制传统的多边形，还能绘制非闭合的多边形，各部分不相连的多边形等等。


对于一般的几何问题，使用`Polygon`就足够了，只有在需要表达一些图形的组合或序列时，才会用到`Polygram`。


`manim`中关于`Polygon`和`Polygram`的模块主要有4个：


1. `Polygon`：任意多边形
2. `RegularPolygon`：任意**正**多边形
3. `Polygram`：广义的多边形
4. `RegularPolygram`：广义的**正**多边形


`Polygon`和`Polygram`其实也可以绘制**正**多边形，只不过用`RegularPolygon`和`RegularPolygram`会更加方便。


![](https://img2024.cnblogs.com/blog/83005/202409/83005-20240913092115417-1310539022.png)


这4个模块的继承关系如上图所示。


# 1\. 主要参数


`Polygon`的参数很简单，就是提供一系列的顶点坐标。


绘制时会依照提供的顶点顺序依次连线，最后一个点会连接第一个点，形成一个闭合的多边形。




| **参数名称** | **类型** | **说明** |
| --- | --- | --- |
| vertices | Point3D | 多边形的顶点列表 |


`RegularPolygon`的参数也很简单：




| **参数名称** | **类型** | **说明** |
| --- | --- | --- |
| n | int | 正多边形的边数 |


`Polygram`的参数是多组的顶点，每组有多个顶点，与之相比，`Polygon`的参数只有一组顶点。




| **参数名称** | **类型** | **说明** |
| --- | --- | --- |
| vertex\_groups | Point3D | 多组顶点列表，如果只有一组顶点，那么图形和`Polygon`一样 |


`RegularPolygram`的参数有：




| **参数名称** | **类型** | **说明** |
| --- | --- | --- |
| num\_vertices | int | 顶点的个数 |
| radius | float | 图形外接圆的半径 |
| density | int | 跳跃多少个顶点来连接 |
| start\_angle | float | 第一个顶点的角度 |


`RegularPolygon`比较简单，就是顺序连接各个顶点形成多边形，


而`RegularPolygram`有个`density`参数，可以控制跳跃几个顶点来连接。


设置`density=1`的话，`RegularPolygram`和`RegularPolygon`的图形是一样的，后面示例中详细演示。


# 2\. 主要方法


`Polygram`作为最通用的多边形，提供了3个方法。




| **名称** | **说明** |
| --- | --- |
| get\_vertex\_groups | 以分组的形式获取多变形的所有顶点坐标 |
| get\_vertices | 获取多变形的所有顶点坐标 |
| round\_corners | 调整多边形角的曲率 |


`get_vertex_groups`和`get_vertices`主要区别在于：


`get_vertex_groups`以分组的形式返回顶点坐标，这对于`Polygram`模块比较有用，因为`Polygram`模块的参数可以传入多组顶点；


`get_vertices`则是将所有的坐标作为一个列表返回出来。


`round_corners`用来调整多边形尖角的曲率。



```
# 创建3个广义正六边形
p1 = RegularPolygram(6)
p2 = RegularPolygram(6)
p3 = RegularPolygram(6)

# p2的尖角曲率设为0.1
p2.round_corners(radius=0.1)

# p3的尖角曲率设为0.3
p3.round_corners(radius=0.3)

```

![](https://img2024.cnblogs.com/blog/83005/202409/83005-20240913092115421-890736068.gif)


其他3个模块没有什么重要的方法。


# 3\. 使用示例


## 3\.1\. 多边形示例


多变形就是按照传入的顶点的顺序逐个连接成一个闭合图形。



```
# 凸多边形
points = [
    LEFT * 2.5,
    LEFT * 1.5 + UP,
    LEFT * 0.5,
    LEFT * 0.5 + DOWN * 1.5,
    LEFT * 2.5 + DOWN * 1.5,
]
Polygon(*points)

# 凹多边形
points = [
    RIGHT * 0.5 + UP,
    RIGHT * 1.5 + DOWN,
    RIGHT * 2.5 + UP,
    RIGHT * 2.5 + DOWN * 1.5,
    RIGHT * 0.5 + DOWN * 1.5,
]
Polygon(*points)

```

![](https://img2024.cnblogs.com/blog/83005/202409/83005-20240913092115390-1101665038.gif)


## 3\.2\. 正多边形


正多边形最简单，只要传入边的数量即可。



```
RegularPolygon(n=6)
RegularPolygon(n=8)
RegularPolygon(n=12)

```

![](https://img2024.cnblogs.com/blog/83005/202409/83005-20240913092115447-677504077.gif)


## 3\.3\. 广义多边形


广义多边形更像是多个多边形的组合，它可以传入多个组的的顶点，然后根据每个组的顶点来构造图形。


下面的示例中，第一个图形有3个组顶点，第二个图形有2个组顶点。



```
group_points = [
    [[-2.5,0,0], [-1.5,1,0], [-0.5,0,0]],
    [[-2,0,0], [-2,-1.5,0]],
    [[-1,0,0], [-1,-1.5,0]],
]
Polygram(*group_points)

group_points = [
    [[0.5,0,0], [1.5,1,0], [2.5,0,0]],
    [[0.5,-1,0], [1.5,0,0], [2.5,-1,0]],
]
Polygram(*group_points)


```

![](https://img2024.cnblogs.com/blog/83005/202409/83005-20240913092115447-635357597.gif)


## 3\.4\. 广义正多边形


广义正多边形可以调整顶点的连接顺序（通过属性`density`），逐个连接时，和普通正多边形是一样的。



```
# 正九边形，逐个连接顶点
RegularPolygram(9, density=1)

# 正九边形，隔一个顶点连接
RegularPolygram(9, density=2)

# 正九边形，隔两个顶点连接
RegularPolygram(9, density=3)

```

![](https://img2024.cnblogs.com/blog/83005/202409/83005-20240913092115403-626136974.gif)


# 4\. 附件


文中完整的代码放在网盘中了（`polygon02.py`），


下载地址: [完整代码](https://github.com) (访问密码: 6872\)


