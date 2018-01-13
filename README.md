# DataVis_Project
Data Visualization with D3.js

## 1.概要

1. 数据集：[棒球数据](https://s3.amazonaws.com/udacity-hosted-downloads/ud507/baseball_data.csv)，包含1157名棒球手的数据集，包括他们的用手习惯（左手还是右手）、身高（寸）、体重（磅）、击球率和全垒得分。
2. 本项目通过可视化展示这些变量对于球手的表现差异，主要表达两个观点
	* 1. 大部分棒球手习惯使用右手
	* 2. 棒球手身高集中分布在69-75英寸，体重分布集中在160-200磅间
	* 3. 可以观察到使用左手和双手的选手明显得分更高



## 2.设计

1. 首图创建了球手用手习惯对于全垒得分的表现差异
2. 添加了变量按钮（身高，体重，击球率），使用颜色区分选手用手习惯
3. 可视化图形选取身高、体重、击球率与全垒得分的关系，讲述不同体型（身高体重）的选手的用手习惯与比赛表现（全垒得分）的差异

*** 
update 2018/01/13

4. 可视化图形设计

| 图表类型 | x 轴 | y 轴 | 颜色 | 图例 |
| 分组柱状图 | handedness/weight/height/avg | y1: Average HR; y2: Total Number of Players | handedness | handedness |

5. 可视化动画与互动： 添加了变量按钮, 过渡动画提供读者进行切换变量来进行探索互动
6. 将堆叠柱形图改为分组柱形图（根据反馈更新）
7. 添加了分组选手总数的折线图，为平均全垒得分与左右手的关系提供参考（根据反馈更新）


## 3.反馈
1. 可视化中的初始图没有问题。但是当我点击height, weight, avg三个标签时出现了新的堆柱形图。你的做法是将B L R三种的average home run得分堆叠在了一起，但是我们更关注的是这三者的差异，而不是总体，而且这三者的和本身并没有意义，因此推荐你使用分组柱形图的方式，而不是堆柱形图。
2. 此外，因为你用到的是聚合数据平均值，最好能够给出聚合后每组的人数，使信息更加完整。（因为组内人数越多，平均值越具有可信度，不容易受到极值的影响。）

## 4.资源

1. [dimple ducumentation](https://github.com/PMSI-AlignAlytics/dimple)
2. [dimple exmaple](http://dimplejs.org/examples_index.html)
3. [d3 ducumentation](https://github.com/d3/d3/blob/master/API.md)