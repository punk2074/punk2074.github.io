---
title: inside_creator_2_hexagon_terrain
date: 2021-02-20 11:28:33
tags: [Creator,Game]
---
![cover](./3.jpg)
```  
cocos creator3.x 之六边形地形
```
<!-- more -->

#### 地形网格
游戏，少不了地图，而地图就需要有坐标，有正方形、六边形等，这里采用六边形是因为任何对于计算六边形到六边形的距离都是一致的，而正方形一边少，二会出现次相邻情况.如下图，但是其实也各有优劣，视项目情况而定吧。     
![地形距离比较](./1.jpg)  

#### 地形制作  
* 制作六边形地形，为了便于调试，制作两个quad地形
* 地图设定及相关代码处理
* 使用射线检测来添加触摸地形快操作  

#### 效果展示
![效果图](./2.jpg) 
#### 参考
* [地形Terrain](https://docs.cocos.com/creator/3.0/manual/zh/editor/terrain/)
* [六边形设计(中文)](https://indienova.com/indie-game-development/hex-grids-reference/)
* [六边形(原版英文)](https://www.redblobgames.com/grids/hexagons/)  
* [射线检测](https://docs.cocos.com/creator/3.0/manual/zh/physics/physics-raycast.html?h=screenpointtoray)  
* [github示例](https://github.com/tim-punk/inside_creator/tree/master/2_hexagon_terrain)