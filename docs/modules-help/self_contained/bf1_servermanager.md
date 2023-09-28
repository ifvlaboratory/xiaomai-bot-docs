# BF1服务器管理

Placeholder  
參數說明: ()代表是必選的 []代表是可選的  

## 查询服务器

### 指令

`-f -fwq -FWQ -服 -服务器 -狐务器 -负无穷`  

### 用法

-f \[群组名\]\[服务器序号\]  
上述查询指令后面可以加上 群组名和服务器序号 用以查詢對應伺服器的信息  

### 示例

`-服务器 sakula1` 查询群组`sakula`的第一个服务器的详情  
`-f1` 查询当前QQ群绑定的服务器详情  

## 查询服内群友

### 指令

`-谁在玩 -谁在捞`  

### 用法

-谁在玩 \[群组名\]\[服务器序号\]  

### 示例

`-谁在玩sakula1` 查询群组`sakula`的`1`服有哪些群友在玩  
`-谁在捞1` 查询当前QQ群绑定的`1`服有哪些群友在玩  

## 查询玩家列表

### 指令

`-玩家列表 -playerlist -pl -lb`  

### 用法

-玩家列表 \[群组名\]\[服务器序号\]  

### 示例

`-pl sakula1` 查询群组`sakula`的`1`服玩家列表  
`-lb1` 查询当前QQ群绑定的`1`服玩家列表  

## 刷新 session

### 指令

`-refresh`  

### 用法

-refresh \[群组名\]\[服务器序号\]  

### 示例

`-refresh1` 刷新当前QQ群绑定的`1`服的session  
`-refresh sakula1` 刷新群组`sakula`的`1`服的session  

## 踢出玩家

### 指令

`-kick -踢 -k -滚出`  

### 用法

-kick \[群组名\]\(服务器序号\) \(玩家名\) \[原因\]  

### 示例

`-kick sakula1 shlsan13 你好` 在群组`sakula`的`1`服踢出玩家`shlsan13` 原因爲`你好`  
`-k1 shlsan13` 在当前QQ群绑定的`1`服踢出玩家`shlsan13` 原因爲`違反規則`\(默認理由\)  

## 封禁玩家

### 指令

`-ban -封禁`  

### 用法

-ban \[群组名\]\(服务器序号\) \(玩家名\) \[原因\]  

### 示例

`-ban sakula1 shlsan13 你好` 在群组`sakula`的`1`服封禁玩家`shlsan13` 原因爲`你好`  
`-ban1 shlsan13 你好` 在当前QQ群绑定的`1`服封禁玩家`shlsan13` 原因爲`你好`  

## 解封玩家

### 指令

`-unban -uban -解封`  

### 用法

-unban \[群组名]\(服务器序号\) \(玩家名\)  

### 示例

`-unban sakula1 shlsan13` 在群组`sakula`的`1`服解封玩家`shlsan13`  
`-unban1 shlsan13` 在当前QQ群绑定的`1`服解封玩家`shlsan13`  

## 全部封禁

### 指令

`-banall -ba`  

### 用法

-banall \[群组名\] \(玩家名\) \[原因\] 全部封禁时不能加服务器序号只能(必须)写群组名  

### 示例

`-ba sakula 你好` 在群组`sakula`的所有伺服器封禁玩家`shlsan13`  原因爲`你好`  
`-basakula shlsan13 你好` 在当前QQ群绑定的群组的所有伺服器封禁玩家`shlsan13`  原因爲`你好`  

## 全部解封

### 指令

`-unbanall -uba`  

### 用法

-unbanall \[群组名\] \(玩家名\)  

### 示例

`-uba sakula shlsan13` 在群组`sakula`的所有伺服器解封玩家`shlsan13`  
`-ubasakula shlsan13` 在当前QQ群绑定的群组的所有伺服器解封玩家`shlsan13`  

## 检查是否封禁玩家

### 指令

`-checkban`  

### 用法

-checkban \[群组名\] \(玩家名\)  

### 示例

`-checkban sakula shlsan13` 查询群组`sakula`是否封禁了玩家`shlsan13`  
`-checkban shlsan13` 查询当前QQ群绑定的群组是否封禁了玩家`shlsan13`  

## 清理 BAN 位

### 指令

`-清理ban位 -清ban`  

### 用法

-清ban \[群组名\]\(服务器序号\) \[数量\]  

### 示例

`-清理ban位 sakula1 100` 清理群组`sakula`的100個BAN位  
`-清ban1` \(当不指定数量时默认全部清理\)  

## 换边

### 指令

`-move -换边 -挪`  

### 用法

-move \群组名\] \(服务器序号\) \(玩家名\) \(队伍ID\)  
1=進攻方 2=防守方  

### 示例

`-move sakula1 shlsan13 1` 在群组`sakula`的`1`服將玩家`shlsan13`移動到`隊伍1`  
`-move1 shlsan13 2` 在当前QQ群绑定的`1`服將玩家`shlsan13`移動到`隊伍2`  

## 换图

### 指令

`-map -换图 -切图`  

### 用法

-map \[群组名\] \(服务器序号\) \(地图名或序号\)  

### 示例

`-map sakula1 要塞`  
`-map1 重开`  

## 图池换图

### 指令

`-图池 -maplist -地图池`  

### 用法

-maplist \[群组名\] \(服务器序号\)  

### 示例

`-图池 sakula1`  
`-maplist1`  

## 加 VIP

### 指令

`-vip -v -加v -上v`  

### 用法

-vip \[群组名\] \(服务器序号\) \(玩家名\) \[时间\]  
时间单位爲天，可为负数，不指定則時間無限  

### 示例

`-vip sakula1 shlsan13 3`  
`-vip1 shlsan13 -3`  

## 下 VIP

### 指令

`-unvip -uvip -删v -下v -减v`  

### 用法

-unvip \[群组名\] \(服务器序号\) \(玩家名\)  

### 示例

`-unvip sakula1 shlsan13`  
`-unvip1 shlsan13`  

## 检查 VIP

### 指令

`-checkvip`  

### 用法

-checkvip \[群组名\] \(服务器序号\)  
行动服用于自动将缓存VIP生效 删除,并重开当前地图(非首图不重开但提示重开)，征服会清理VIP  

### 示例

`-checkvip sakula1`  
`-checkvip1`  

## VIP 列表

### 指令

`-viplist -vip 列表 -vl`  

### 用法

-viplist \[群组名\] \(服务器序号\)  

### 示例

`-vl1`  
`-vl sakula1`  

## BAN 列表

### 指令

`-banlist -ban 列表 -bl -封禁列表 -封禁list`  

### 用法

-banlist \[群组名\] \(服务器序号\)  

### 示例

`-bl sakula1`  
`-bl1`  

## ADMIN 列表

### 指令

`-adminlist -管理列表 -al`  

### 用法

-adminlist \[群组名\] \(服务器序号\)  

### 示例

`-al sakula1`  
`-al1`  
