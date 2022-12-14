<!--
 * @Coding: utf-8
 * @Author: vector-wlc
 * @Date: 2021-09-25 16:18:59
 * @Description: 
-->
# 冰三和铲除函数

## 冰三
由于 PvZ 序号大小的影响，植物的生效倒计时会发生 1cs 的波动，为了解决这个问题，AvZ 提供了设定植物生效时间的功能。

**请不要滥用此功能，这可能会破坏游戏规则**


`SetPlantActiveTime` 函数参数的意义是将指定类型的植物的生效时间设置为  最近一次的 `SetTime` 设定的时间点的参数时间后，使用了此函数后冰三这个操作是基本不可能失败的。

```C++
// 修正寒冰菇生效时间点到 (-599, 1) 的 298cs 后
SetTime(-599, 1);
SetPlantActiveTime(ICE_SHROOM, 298);
```



## 铲除
铲除操作由函数 Shovel 实现

```C++
// 铲除4行6列的植物,如果植物有南瓜保护默认铲除被保护植物
Shovel(4, 6);

// 铲除4行6列的植物,如果植物有南瓜保护铲除南瓜
Shovel(4, 6, true);

// 铲除3行6列，4行6列的植物
Shovel({{3, 6},{4, 6}});
```

[上一篇 存冰类](./ice_filler.md)

[目录](../catalogue.md)

[下一篇 修补植物类](./plant_fixer.md)