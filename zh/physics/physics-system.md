# 物理系统

物理系统（PhysicsSystem）是一个模拟真实物理行为的系统，它负责对物理世界中的元素进行物理计算，比如计算各物体是否产生碰撞，以及物体的受力情况。所有元素计算完成后，还会更新到场景世界中，从而使游戏对象产生相应的物理行为。

目前 Cocos Creator 3D 中物理计算所处的流程 ：  所有 Update 结束后 → 物理计算 → 开始渲染

场景世界与物理世界，如图：
![场景世界与物理世界](img/SceneAndPhysics.png)

## 物理系统属性与接口

目前物理系统的属性暂时只能通过代码去设置，以后将会增加新的面板，使得某些物理系统的相关属性设置更好友好，请留意更新公告。

属性 | 解释
---|---
**enable** |  是否开启物理系统，默认为 true
**allowSleep** |  是否允许物理系统自动休眠，默认为 true
**maxSubStep** |  物理每帧模拟的最大子步数，默认为 2
**deltaTime** |  物理每步模拟消耗的时间，注意不是每帧，默认为 1 / 60
**gravity** |  物理世界的重力值，默认为 (0, -10, 0)

目前可以用此方式获取到物理系统实例： `PhysicsSystem.ins`

**注：Builtin 中不支持以上物理模拟相关的属性**。

---

继续前往 [物理组件](physics-component.md) 说明文档。
