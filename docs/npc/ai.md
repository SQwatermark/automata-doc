# AI

Automata模组不提供复杂的战斗AI设计，仅提供一些可以快速创建AI的工具。和几种常用的行为模式。

## 行动模式

### 无

不提供任何行为，在不使用脚本的情况下，NPC不会有任何行为。

如果需要使用脚本修改NPC的行为，建议使用这种行动模式。

可以指定其播放的动画。

### 站桩

原地不动，且不可推动，如果位置离开原位，将直接传送回原位。

如果玩家与其交互，将转向玩家。

可以指定其播放的动画。

### 游荡

在指定半径范围内游走。

可以指定其游走速度、行走状态播放的动画、站立状态播放的动画。

### 路径移动

## 通过脚本自定义AI

NPC加载时会调用init方法进行初始化，此时可初始化它的AI。

可通过NpcEntity的setLookControl，setMoveControl，setJumpControl，setPathNavigation方法设置实体的看、移动、跳跃和寻路控件。

Automata脚本扩展提供了几种常用控件，你也可以编写自己的模组，继承原版类以实现自己的控件。

Automata脚本扩展提供的控件有：

LookControl：

- 暂无

MoveControl：

- 普通移动
- 飞行移动
  - 最大转角
  - 是否悬停

JumpControl：

- 暂无

PathNavigation：

- 地面
  - 是否避免阳光
- 飞行
- 游泳

Automata提供了一套便于让脚本和Java代码协同工作的AI实现方式。

TODO 我自己都忘了这玩意怎么用了

```java
// 开始某个行为
void startAction(@NotNull BaseAction action);

// 开始某个行为
void startAction(@NotNull String key, @NotNull BaseAction action);

// 停止某个行为
void stopAction(@NotNull String key);
```