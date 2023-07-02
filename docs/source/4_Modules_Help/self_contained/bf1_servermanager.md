# 战地1服务器管理

## 描述

管理战地一服务器的插件  

## 用法

[]代表该参数是必选的 ()代表该参数是可选的 注意指令空格  

### 刷新 session

```text
-refresh
```

### 查询服务器

```text
-服务器 -狐务器
-f
```

### 查询服务器玩家

```text
-谁在玩[序号]
-玩家列表[序号]
-pl[序号]
```

### 查询管理

```text
-adminlist[序号]
-al[序号]
-管理列表[序号]
```

### 查询日志

```text
-bf群组日志 (qq号)
```

### 踢出玩家

```text
-k(序号) [玩家ID] (原因)
-kick(序号) [玩家ID] (原因)
-踢(序号) [玩家ID] (原因)
-sk [玩家ID] (原因)
```

### 换边玩家

```text
-换边[序号] [玩家ID]
-挪[序号] [玩家ID]
-move[序号] [玩家ID]
```

### VIP 操作

```text
-vn [玩家ID] (天数) (天数可选不填为永久可为负数)
-uvn [玩家ID]
-清v[序号]
-viplist[序号]
v=上v=vip=加v uv=unvip=下v=删v=减v viplist=vl=vip列表 清v=清vip=清理vip
```

### 封禁操作

```text
-ban[序号] [玩家ID] 原因(可省)
-unban[序号] [玩家ID]
-banall [玩家ID] 原因(可省)
-unbanall [玩家ID]
-清ban[序号] (0~200不填默认200)
-banlist[序号]
-checkban 玩家id
b=ban=封禁 ub=unban=解封 banlist=bl=ban列表 清ban=清理ban位
```

### VBAN 操作

```text
-vban[序号] [玩家ID] 原因(可省)
-unvban[序号] [玩家ID] 原因(可省)
-vbanlist[序号]
vban=vb=加vban unvban=uvb=减vban vbanlist=vban列表
```

### 换图操作

```text
-换图[序号] <地图序号/地图名>
-图池[序号]
换图=切图=map 地图池=图池=maplist
```

## 示例

```text
-f
-k1 shlsan13 test
-ban1 shlsan13 test
-banall shlsan13 test
-unbanall shlsan13 test
-v1 shlsan13 3
-v1 shlsan13 -3
-uv1 shlsan13 3
-map1 要 (图名可以只打一个字)
-map1 重开
-vban1 shlsan13 test
-unvban1 shlsan13 test
```

