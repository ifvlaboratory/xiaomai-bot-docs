# BF1群組管理

Placeholder

## 增改查刪

-bfg 新建(new)/删除(del)/信息(info) 群组名
如: -bfg info sakula  

-bfg 改名(rename) 群组名 new_name
如: -bfg rename sakula sakula2  

## 绑定解绑

-bfg 群组名 绑服#(bind#)服务器序号 服务器gameid
如: -bfg sakula bind#1 123123123  

-bfg 群组名 解绑#服务器序号
如: -bfg sakula 解绑#1  

-bfg 群组名 绑群 QQ群号
如:-bfg sakula 绑群 123123  

-bfg 解绑群 QQ群号
如:-bfg 解绑群 123123  

## 权限管理

添加/删除 管理/服主, aa为添加管理员,ao为添加服主,del为删除权限
-bfg 群组名 aa/ao/del qq号(可以为@元素,可为多个用空格隔开)
如:-bfg sakula aa @你 @他  

-bfg 群组名 权限列表(permlist)
如:-bfg sakula permlist  

## 帐号管理

指令前缀:-bf服管账号 = -bfga  

查询服管帐号列表:  
-bf服管账号列表  = -bfal  

登录/新建帐号: 
-bf服管帐号 登录 玩家名 remid=xxx,sid=xxx  
如:-bfga login SHlSAN13 remid=xxx,sid=xxx  

删除:  
-bf服管帐号 删除 帐号pid  
如:-bfga del 123123  
(123123为获取到的帐号pid)  

信息:
-bf服管帐号 信息 帐号pid
如:-bfga info 123123  

## 群组绑定/解绑

-bf群组 群组名#服务器序号 使用服管(use) 帐号pid
如:-bfg sakula#1 use 123123
(绑定指定服)  

-bf群组 群组名 使用服管(use) 帐号pid
如:-bfg sakula use 123123
(绑定所有服)  

-bf群组 群组名 #服务器序号 解绑服管
如:-bfg sakula #1 解绑服管  

-bf群组 群组名 解绑服管
如:-bfg sakula 解绑服管  

## vban

-bf群组 群组名 创建vban#序号
如:-bfg sakula 创建vban#1  

-bf群组 群组名 vban信息
如:-bfg sakula vban信息  

-bf群组 群组名 删除vban#序号
如:-bfg sakula 删除vban#1  

-bf群组 群组名 配置vban#序号 gid=xxx,token=xxx
如:-bfg sakula 配置vban#1 gid=123,token=abc  

## 服管日志

前缀:-bflog/-服管日志  
操作(可选):"kick", "ban", "unban", "change_map", "vip", "unvip",  
                "踢出", "封禁", "解封", "换图", "上v", "下v"  
群组名(可选)  
可选参数:  
服务器序号:i/index  
操作人qq:q/qq  
被操作人pid: p/pid  
名字:n/name  

参数是由 减号'-' + 参数名(如你想查qq就是q/qq) + 可选等号(=) +参数(qq就是对应qq)  
所以假如你想查qq=123的操作日志,对应参数指令就是 -q=123  
同理得-i=5  
由此我们可以得出以下指令  
-bflog 换图 -i=1 -q=123  
这个指令是:查询qq为123的人在1服换图的日志  
-bflog -n=123  
这个指令是:名字为123的玩家在整个群组被操作的日志(包括上下v封禁踢出)  
