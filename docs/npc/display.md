# 显示

## 模型

Automata模组主要支持基岩版实体模型

Automata的模型不需要提前下发给客户端，而是由模组通过网络传输给客户端，客户端进行缓存。

TODO 从客户端直接上传模型

## 动画

Automata有四个动画槽位并行播放。

TODO 提供脚本接口

```java
// 在第一个槽位循环播放一段动画
void playAnimation(@NotNull String animationKey);

/**
 * index从0到3，分别表示四个槽位
 */
void playAnimation(@NotNull String animationKey, int index);

/**
 * loopType为0表示循环播放，loopType为1表示播放一次，loopType为2表示停止在最后一帧（似乎没有实现？）
 */
void playAnimation(@NotNull String animationKey, int index, int loopType);

/**
 * 在第一个槽位播放一段动画一次，接着循环播放另一段动画
 */
void playAndLoop(@NotNull String animationToPlayOnce, @NotNull String loopAnimation);

/**
 * 在指定槽位播放一段动画一次，接着循环播放另一段动画
 */
void playAndLoop(@NotNull String animationToPlayOnce, @NotNull String loopAnimation, int index);

// TODO 清除指定槽位的动画
```