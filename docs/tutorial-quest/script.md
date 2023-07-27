---
sidebar_position: 5
---

# 脚本（未实现）

## 脚本事件

### 任务开始

``` java
void questStart(Event event) {
    // ...
}

class Event {
  ServerPlayer player;
}
```

### 任务结束

``` java
void questEnd(Event event) {
    // ...
}

class Event {
  ServerPlayer player;
  int id; // 结束节点的ID
}
```

### 任务加载

任务加载会在任务开始后执行一次，也会在正在进行该任务的玩家进入服务器时执行一次。

``` java
void questLoad(Event event) {
    // ...
}

class Event {
  ServerPlayer player;
}
```

### 任务卸载

任务卸载会在任务结束后执行一次，也会在正在进行该任务的玩家离开服务器时执行一次。

``` java
void questUnload(Event event) {
    // ...
}

class Event {
  ServerPlayer player;
  int id; // 结束节点的ID
}
```

### 任务目标开始

``` java
taskStart(event) {
    // ...
}

class Event {
  ServerPlayer player;
  int id; // 任务目标节点的ID
}
```

### 任务目标结束

``` java
void taskEnd(event) {
    // ...
}

class Event {
  ServerPlayer player;
  int id; // 任务目标节点的ID
}
```

### 任务目标加载

任务目标加载会在任务目标开始后执行一次，也会在正在进行该任务目标的玩家进入服务器时执行一次。

``` java
void taskLoad(Event event) {
    // ...
}

class Event {
  ServerPlayer player;
  int id; // 任务目标节点的ID
}
```

### 任务目标卸载

任务目标卸载会在任务目标结束后执行一次，也会在正在进行该任务目标的玩家离开服务器时执行一次。

``` java
void taskUnload(Event event) {
    // ...
}

class Event {
  ServerPlayer player;
  int id; // 任务目标节点的ID
}
```

## 脚本API

### 开始任务

仅可为在线的玩家开始任务，且该玩家不能正在进行该任务。

```java
AutomataApi.startQuest(UUID playerId, String questId);
```

### 结束任务

仅可为在线的玩家结束任务，且该玩家必须正在进行该任务。

```java
// endId是结束节点的ID
AutomataApi.completeQuest(UUID playerId, String questId, int endId);
```

## 待定

正在考虑是否应当开放这些接口，用起来可能有严重的问题

### 开始任务目标

```java
AutomataApi.startTask(UUID playerId, String questId, int taskId);
```

### 结束任务目标

```java
AutomataApi.completeTask(UUID playerId, String questId, int taskId);
```

## 模组API

### 注册新Task类型

TODO