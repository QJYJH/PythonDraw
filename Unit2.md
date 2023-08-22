![image](https://github.com/QJYJH/PythonDraw/assets/77378456/eda5c557-bce8-48df-aa12-a3223da9e42f)# 工具：　Matplotlib <br>
## 部分属性：用 Matplotlib 绘制图形的主要图形元素包括画布（figure）、坐标图形（axes）、轴（axis）和艺术对象（aritist）
如图 2-1-1 所示。其中坐标图形中包括大部分绘图所需的图层属性，
如图名（title）、刻度（tick）、刻度标签（tick label）、轴标签（axis label）、轴脊（spine）、图例（legend）、网格（grid）、线（line）和数据标记（marker）等 <br>
Matplotlib包含基础类（primitive）元素和容器类（container）元素。基础类元素包括常见的点（point）、
线（line）、文本（text）、网格（grid）、标题（title）、图例（legend）等；容器类元素则是指
一种或多种基础类元素的合集，主要包括图形、坐标图形、轴和刻度

![image](https://github.com/QJYJH/PythonDraw/assets/77378456/1d81762c-0483-421b-966c-4e2a6e814874)


## 图层顺序：
在同一个坐标图形中绘制不同的数据图层时，
Matplotlib 可通过设置每个绘图函数中的 zorder 参数来设定不同的图层。不同的艺术对象在坐
标图形中的默认图层顺序如表 2-1-1 所示


![image](https://github.com/QJYJH/PythonDraw/assets/77378456/b9b41d8b-379a-4e44-8935-d0cd48eed1f4)


## 多子图绘制：
### 1．subplot() 函数<br>
Matplotlib 提供的 subplot() 函数可以对当前画布对象添加单个子图，且每次添加子图都会
规定其位置顺序。示例代码如下。<br>
1. import matplotlib.pyplot as plt<br>
2. ax1 = plt.subplot(212)<br>
3. ax2 = plt.subplot(221)<br>
4. ax3 = plt.subplot(222)<br>

![image](https://github.com/QJYJH/PythonDraw/assets/77378456/3e70b13f-4599-422a-adfa-37d5fb778442)

### 3．subplots() 函数
Matplotlib 提供的 subplots() 函数是常见的用于绘制子图的函数。该函数的语法格式如下。<br>
subplots(nrows, ncols, sharex, sharey)<br>
该函数的第 1 个参数 nrows 表示绘制子图的行数，第 2 个参数 ncols 表示绘制子图的列数，
行数与列数的乘积即绘制的总子图数，第 3 个参数 sharex 可以用来设定是否共享 X 轴，第 4
个参数 sharey 可以用来设定是否共享 Y 轴。该函数会返回一个坐标数组对象，该对象用于每
个子图的单独绘制。示例代码如下。<br>
1. fig, axs = plt.subplots(2, 3, sharex=True, sharey=True)<br>
2. axs[0,0].text(0.5, 0.5, "subplots(0,0)")<br>
3. axs[0,1].text(0.5, 0.5, "subplots(0,1)")<br>
4. axs[0,2].text(0.5, 0.5, "subplots(0,2)")<br>
5. axs[1,0].text(0.5, 0.5, "subplots(1,0)")<br>
6. axs[1,1].text(0.5, 0.5, "subplots(1,1)")<br>
7. axs[1,2].text(0.5, 0.5, "subplots(1,2)")<br>

![image](https://github.com/QJYJH/PythonDraw/assets/77378456/5a8ef471-4628-4ee4-a1ea-310d410df620)


### 5．subplot2grid() 函数
Matplotlib 中的 subplot2grid() 函数可以实现对不规则多子图的绘制，即在当前画布对象上
绘制网格（grid），网格可用于在特定位置绘制布局和大小不同的子图对象。subplot2grid() 函
数的语法格式如下。<br>
subplot2grid(shape, location, rowspan/colspan)<br>
该函数的第 1 个参数 shape 规定了的网格的行数和列数，第 2 个参数 location 决定了子图
在网格内的行号和列号，第 3 个参数为 rowspan 或 colspan，它们分别规定了每个子图向下跨
越的行数和向右跨越的列数，也就实现了大小不一的子图的绘制。示例代码如下。<br>
1. import matplotlib.pyplot as plt<br>
2. fig = plt.figure()<br>
3. ax1 = plt.subplot2grid((3, 3), (0, 0), colspan=3)<br>
4. ax2 = plt.subplot2grid((3, 3), (1, 0), colspan=2)<br>
5. ax3 = plt.subplot2grid((3, 3), (1, 2), rowspan=2)<br>
6. ax4 = plt.subplot2grid((3, 3), (2, 0))<br>
7. ax5 = plt.subplot2grid((3, 3), (2, 1))<br>

![image](https://github.com/QJYJH/PythonDraw/assets/77378456/357ec619-f47d-4f3b-bd1e-176fc8b198d8)


## 保存图片：
![image](https://github.com/QJYJH/PythonDraw/assets/77378456/8ac37936-2b3f-4801-ad32-28ed0d3f1f84)





