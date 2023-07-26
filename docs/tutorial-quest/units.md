---
sidebar_position: 4
---

# 节点

任务的所有输入端口都只能有一个输入，输出端口可以有任意多个输出。

## 开始

每个任务只有一个开始节点，由新建任务时自动创建，无法通过编辑器添加或删除开始节点。

## 结束

每个任务可以有多个结束节点，当任意一个结束节点的前置节点完成时，该任务会立即完成。

TODO 结束节点后边可以接行为节点

## 任务目标节点

TODO 共通属性：是否隐藏，如果为是，则开始和完成任务目标时玩家不会收到提示，玩家任务界面中也不会显示该任务目标。

共通属性：自定义描述

### 对话



### 击杀NPC

### 世界

## 流程控制节点

### 或（流程控制）

完成条件：两个前置节点都已完成

### 且（流程控制）

完成条件：两个前置节点中有任意一个完成

### 阻塞（暂未实现）

完成条件：满足第一个前置节点

它被设计用于制作一些

## 逻辑判断节点（暂未实现）

设计和对话的逻辑判断节点一致

### 或（逻辑判断）

### 且（逻辑判断）

### 非

### 脚本（逻辑判断）

## 行为节点（全部暂未实现）

### 物品

布尔值：取走/给予

正整数：数量

物品（物品怎么做输入？）

### 脚本（行为）