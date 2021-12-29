---
title: inside_creator_1_plugin
date: 2021-02-15 12:19:41
tags: [Creator,Game]
---

```  
cocos creator3.x 之插件编写
```
<!-- more -->
#### 关于插件
一般对于游戏开发者，大部分都会与excel打交道，策划给角色或者怪物配置的血量、等级、技能等。关卡信息、奖励道具等。还有美术给的动作名称、技能帧等，包括一些活动配置等游戏中用得到并且在上线前频繁修改的数据，对于这些数据而言，有一个规范、容易编辑、更新的工具对整个项目来说是事半功倍的效果。特此，插件就派上场了。

#### 插件制作  
插件的制作参考以下链接  
* [深入 Cocos Creator 3.0 的插件扩展系统](https://mp.weixin.qq.com/s?__biz=MjM5ODAxNTM2NA==&mid=2659664592&idx=1&sn=9793c8f33cdf2c73b4cbaa9af9944d45&chksm=bda2da3b8ad5532d18296c170e3953f66c0e85ee715f3d75f2e1cafe2219a033cd44c9257aac&scene=178&cur_album_id=1761139408994385920#rd)  
* [扩展编辑器](https://docs.cocos.com/creator/3.0/manual/zh/editor/extension/readme.html)  

#### 插件使用  
* 目录结构
```
rootdir
  |--client
    |--extensions
    |--assets
      |--scripts
        |--db           #最终生成.ts脚本配置的文件夹
  |--design
    |--excel
      |--role.xls       #配表文件
      |--monster.xls    #配表文件
    |--tool             #导表等工具
```
* 策划安装规范定义好excel表
* 通过Creator中Developer->导出即可  
    1.插件会调用`rootdir\design\tool\export2ts.bat`(mac下sh)执行python脚本  
    2.python会将excel文件夹下xls文件导出至`\rootdir\client\assets\scripts\db\`文件夹中
* python需要安装相关node插件
* 相关说明放在`tool/readme.md`文件内
* [github示例](https://github.com/tim-punk/inside_creator/tree/master/1_plugin)