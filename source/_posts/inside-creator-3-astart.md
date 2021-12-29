---
title: inside_creator_3_astart
date: 2021-02-28 10:07:47
tags:
---
![cover](./1.jpg)
```  
cocos creator3.x 之六边形A* 算法
```
<!-- more -->

#### 导航
地图已经制作完成的话，就需要导航，让角色走到指定位置，并且自动避开障碍物.从而产生了寻路算法，市面上很多算法,A*、D*、导航网格等，但万变不离其宗，都是要找出最近的路。我只拿最简单的A*算法来做

#### A*算法  
1. 将起始节点加入open列表中
2. 判断open节点，空则搜索失败，如果open列表存在目标节点，则搜索成功
3. 根据F = G + H从open列表中找出F最小的节点作为当前节点，并将其加入close列表中
4. 计算当前节点相邻的六个节点(排除障碍物)，组成一组子节点，对每个子节点做判断
    * 如果该节点在close列表中，丢弃。
    * 如果该节点在open列表中，检查当前节点的F值是否更小，如果更小则更新F值，并将父节点设置为当前节点
    * 如果该节点不在open列表中，则将其假如open列表，并计算F值，设置其父节点为当前节点
5. 重复2步骤  

#### 效果展示
![效果图](./2.jpg) 
#### 参考
* [六边形A*算法](https://zhuanlan.zhihu.com/p/112849816)
* [A*算法简述(英文)](https://www.redblobgames.com/pathfinding/a-star/introduction.html)
* [A*算法简述(中文)](https://www.cnblogs.com/iwiniwin/p/10793654.html)  
* [github示例](https://github.com/tim-punk/inside_creator/tree/master/3_find_astar)