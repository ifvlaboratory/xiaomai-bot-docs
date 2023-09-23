# BF1服务器管理

Placeholder

## 查询服务器

-服务器/-fwq/-FWQ/-服/-f/-狐务器/-负无穷
查询服务器详情

### 用法

上述查询指令后面加上 群组名和服务器序号添加服主/管理员
-bfg 群组名 ao/aa @成员 ,ao 为添加服主，aa 为添加管理员,可同时@多个对象删除服主/管理员
-bfg 群组名 del @成员 ,可同时@多个对象

### 示例

````text
-服务器 sakula1 即可查询群组sakula群组的第一个服务器的详情，如果当前QQ群绑定了群组，则可以省略群组名
-f1
````

## 查询服内群友

-谁在玩/-谁在捞 群组名(可选)服务器序号

### 示例

```text
-谁在玩sakula1 1
-谁在捞1
```

## 查询玩家列表

### 用法

-玩家列表/-playerlist/-pl/-lb+群组名(可选)服务器序号

### 示例

```text
-pl sakula1
-lb1
```

## 刷新 session

### 用法

-refresh 群组名(可选)服务器序号

### 示例

```text
-refresh1
-refresh 1
-refresh sakula1
```

## 踢出玩家

### 用法

-kick/-踢/-k/-滚出+可选群组名+服务器序号+空格+玩家名+可选原因

### 示例

```text
-kick sakula1 shlsan13 你好 (注意这里的sakula1的sakula为群组名,1为服务器序号，中间不加任何符号，服务器序号后一定要跟空格)
-k1 shlsan13 你好
```

## 封禁玩家

### 用法

-ban/-封禁+可选群组名+服务器序号+空格+玩家名+可选原因

### 示例

```text
-ban sakula1 shlsan13 你好
-ban1 shlsan13 你好
```

## 解封玩家

### 用法

-unban/-uban/-解封+可选群组名+服务器序号+空格+玩家名,解封不能加原因！

### 示例

```text
-unban sakula1 shlsan13
-unban1 shlsan13
```

## 全部封禁

### 用法

-banall/-ba+空格+群组名+空格+玩家名+可选原因，全部封禁时不能加服务器序号只能(必须)写群组名

### 示例

```text
-ba sakula 你好
-basakula shlsan13 你好
```

## 全部解封

### 用法

-unbanall/-uba+空格+玩家名+群组名，全部解封时不能加服务器序号只能(必须)写群组名

### 示例

```text
-uba sakula shlsan13
-ubasakula shlsan13
```

## 检查是否封禁玩家

### 用法

-checkban+可选群组名+玩家名,不能写服务器序号

### 示例

```text
-checkban sakula xiaoxiao
```

## 清理 BAN 位

### 用法

-清理 ban 位/-清 ban+可选群组名+服务器序号+可选数量，当不指定数量时默认为 200(全部清理)

### 示例

```text
-清理ban位 sakula1 100
-清ban1
```

## 换边

### 用法

-move/-换边/-挪+可选群组名+服务器序号+空格+玩家名+队伍 ID

### 示例

```text
-move sakula1 shlsan13 1
-move1 shlsan13 2
```

## 换图

### 用法

-map/-换图/-切图+可选群组名+服务器序号+空格+地图名/地图序号

### 示例

```text
-map sakula1 要塞
-map1 重开
```

## 图池换图

### 用法

-图池/-maplist/-地图池+可选群组名+服务器序号

### 示例

```text
-图池 sakula1
-maplist1
```

## 加 VIP

### 用法

-vip/-v/-加 v/-上 v+可选群组名+服务器序号+空格+玩家名+可选时间(单位

### 用法

天，可为负数)

### 示例

```text
-vip sakula1 shlsan13 3
-vip1 shlsan13 -3
```

## 下 VIP

### 用法

-unvip/-uvip/-删 v/-下 v/-减 v+可选群组名+服务器序号+空格+玩家名,下 v 时不能写天数

### 示例

```text
-unvip sakula1 shlsan13
-unvip1 shlsan13
```

## 检查 VIP

### 用法

-checkvip+可选群组名+服务器序号

### 示例

```text
-checkvip sakula1
-checkvip1 (行动服用于自动将缓存VIP生效/删除,并重开当前地图(非首图不重开但提示重开)，征服会清理VIP)
```

## VIP 列表

### 用法

-viplist/-vip 列表/-vl+可选群组名+服务器序号

### 示例

```text
-vlsakula1
-vl1
-vl sakula1
```

## BAN 列表

### 用法

-banlist/-ban 列表/-bl/-封禁列表/-封禁 list+可选群组名+服务器序号

### 示例

```text
-bl sakula1
-bl1
-bl sakula1
```

## ADMIN 列表

### 用法

-adminlist/-管理列表/-al+可选群组名+服务器序号

### 示例

```text
-al sakula1
-al1
-al sakula1
```
