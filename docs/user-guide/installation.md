# 安裝

## 简易搭建

1. python3.10+环境, Mirai:[MCL2.1.0](https://docs.mirai.mamoe.net/ConsoleTerminal.html) + 配置[MAH](https://docs.mirai.mamoe.net/mirai-api-http/)  
2. 安装环境依赖(请用推荐方式安装[poetry](https://python-poetry.org/docs/#installation) )  
3. 使用poetry的虚拟环境请直接在bot根目录终端执行:  

```text
poetry install
```

   或者其他虚拟环境(关闭poetry的创建虚拟环境:```poetry config virtualenvs.create false```)  
4. 打开config_demo.yaml文件填写配置信息,填写好后请改名为config.yaml再启动  
5. 启动bot在bot根目录下使用poetry run python main.py  
6. 根据报错缺啥弄啥吧(  

## 使用Docker部署

请先安装Docker
如使用环境变量控制sqlite3位置请同时修改部署文件或指令的映射路径

```sh
bash
git clone https://github.com/g1331/xiaomai-bot                                                          # 下载项目
cd xiaomai-bot                                                                                          # 进入项目目录
docker build -t xiaomai-bot .                                                                           # 构建docker镜像
mv config_demo.yaml config.yaml                                                                         # 请修改配置文件
sqlite3 /xiaomai-bot/config/data.db                                                                     # 创建sqlite数据库
sqlite> .database                                                                                       # 查看数据库
sqlite> .quit                                                                                           # 退出sqlite
docker run -d --name xiaomai-bot\                                                                       # 容器名
      --net=host \                                                                                      # 使用主机网络
      -v /xiaomai-bot/config/config.yaml:/xiaomai-bot/config.yaml \                                     # 挂载配置文件
      -v /xiaomai-bot/config/data.db:/xiaomai-bot/data.db \                                             # 挂载数据库
      -v /xiaomai-bot/data/battlefield:/xiaomai-bot/data/battlefield/ \                                 # 挂载战地一机器人资源
      -v /xiaomai-bot/imgs/random_dingzhen:/xiaomai-bot/modules/self_contained/random_dingzhen/imgs/ \  # 挂载随机丁真图片
      -v /xiaomai-bot/imgs/random_wife:xiaomai-bot/modules/self_contained/random_wife/imgs/ \           # 挂载随机老婆图片
      -v /xiaomai-bot/imgs/random_dragon:xiaomai-bot/modules/self_contained/random_dragon/imgs/ \       # 挂载随机龙图图片
#      -e bot_accounts=bot所使用的账户使用,做分割
#      -e default_account=默认bot账户
#      -e Master=bot管理者账户
#      -e mirai_host=mah服务器
#      -e verify_key=mah服务器验证token
#      -e test_group=发送调试信息的群组
#      -e db_link=sqlite3数据位置
      xiaomai-bot                                                                                       # 运行容器
```

## 使用docker-compose部署

请先安装docker与docker-compose
如使用环境变量控制sqlite3位置请同时修改部署文件或指令的映射路径

```bash
git clone https://github.com/g1331/xiaomai-bot                                                          # 下载项目
cd xiaomai-bot                                                                                          # 进入项目目录
sqlite3 /xiaomai-bot/config/data.db                                                                     # 创建sqlite数据库
sqlite> .database                                                                                       # 查看数据库
sqlite> .quit                                                                                           # 退出
mv config_demo.yaml config.yaml                                                                         # 请修改配置文件，以及docker-compose.yml中的挂载路径
docker-compose up -d                                                                                    # 构建并运行容器
```
