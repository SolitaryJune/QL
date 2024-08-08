
#### 🚩 一键安装青龙面板命令

![img.png](image/img.png)

![img1.png](image/img1.png)
#### 🚩 全自动提交助力码到互助池
![img2.png](image/img2.png)

- 使用方式
```sh
docker exec -it qinglong bash -c "task /ql/jd/1-5.sh && python3 /ql/jd/1-5.py"
docker exec -it qinglong bash -c "task /ql/jd/6-10.sh && python3 /ql/jd/6-10.py"
运行命令后，显示  Please enter your phone (or bot token):
就输入您的注册TG的电话，如果是大陆的格式就是+8613666666666
然后TG接收到验证码填上，再下来，如果TG有密码就输入密码
```
#
- 为防止系统没安装curl，使用不了一键命令，使用一键安装青龙面板命令之前先执行一次安装curl命令

- 安装curl请注意区分系统，openwrt千万别另外安装curl，openwrt本身自带了，另外安装还会用不了
#

- 使用root用户登录ubuntu或者debian系统，后执行以下命令安装curl
```sh
apt -y update && apt -y install curl wget
```

- 使用root用户登录centos系统，后执行以下命令安装curl
```sh
yum install -y curl wget
```
#
- 国外鸡地址，执行下面一键命令安装青龙+依赖+任务+maiark自由选择（安装完毕后再次使用命令可以对应用进行升级）
```sh
bash -c "$(curl -fsSL https://raw.githubusercontent.com/1302557841/QL/main/lang1.sh)"
```
- 国内鸡地址，执行下面一键命令安装青龙+依赖+任务+maiark自由选择（安装完毕后再次使用命令可以对应用进行升级）
```sh
bash -c "$(curl -fsSL https://git.gushao.club/https://raw.githubusercontent.com/SolitaryJune/QL/main/lang1.sh)"
```


## 第二步

#### 🚩 如果上面的命令运行成功会有提示，按提示操作登录面板


- 登录面板后，在‘ 环境变量 ’项添加 WSKEY 或者 PT_KEY

- 添加 wskey 或者 pt_key 都要注意KEY里面的分号，英文分号，记得别省略了，WSKEY和PT_KEY二选一即可

- 格式如下：

```sh
# > 添加 wskey

名称
JD_WSCK

值
pin=您的账号;wskey=您的wskey值;



# > 添加PT_KEY

名称
JD_COOKIE

值
pt_key=您的pt_key值;pt_pin=您的账号;
```

#
#### 🚩 青龙面板安装依赖方法
- ####  依赖管理 --> 添加依赖 --> 依赖类型(NodeJs) --> 自动拆分(是) --> 名称(把下面依赖名称全复制粘贴) --> 确定 
安装不上执行
```sh
 docker exec -it qinglong  cnpm install npm@8.1.2	 -g
```
安装完成后执行
```sh
  docker exec -it qinglong    npm i -g stable
```
```sh
  docker exec -it qinglong   npm config set registry https://registry.npmmirror.com/
```
```sh
date-fns
axios
ts-node
typescript
png-js
crypto-js
md5
dotenv
got
ts-md5
tslib
@types/node
requests
tough-cookie
jsdom
download
tunnel
fs
ws
js-base64
jieba
canvas
ds
canvas
```
#
#### 🚩 单独安装某项的一键脚本


- 一键单独安装docker
```sh
bash -c "$(curl -fsSL https://git.gushao.club/https://raw.githubusercontent.com/1302557841/QL/main/docker.sh)"
```
```
wget -qO- https://get.docker.com/ | sh
```
- 一键安装单独青龙的依赖
```sh
docker exec -it qinglong bash -c  "$(curl -fsSL https://git.gushao.club/https://raw.githubusercontent.com/1302557841/QL/main/npm.sh)"
```
#### 🚩 单独F2拉库
F2库
```sh
ql repo https://github.com/shufflewzc/faker2.git "jd_|jx_|gua_|jddj_|jdCookie" "activity|backUp" "^jd[^_]|USER|function|utils|sendNotify|ZooFaker_Necklace.js|JDJRValidator_|sign_graphics_validate|ql|JDSignValidator" "main"
task disableDuplicateTasksImplement.py
```

yyds
```sh
ql repo https://github.com/okyyds/yyds.git "jd_|jx_|gua_|jddj_|m|jdCookie" "activity|backUp" "^jd[^_]|USER|function|utils|sendNotify|ZooFaker_Necklace.js|JDJRValidator_|sign_graphics_validate|ql|JDSignValidator" "master"
```

feverrun【内部互助版】 (集合库)
【群组地址】https://t.me/proenv
【频道地址】https://t.me/proenvc
【仓库地址】https://github.com/feverrun/my_scripts
```sh
ql repo https://github.com/feverrun/my_scripts.git "jd_|jx_|jddj_|getCookie|getJDCookie" "backUp/activity|backUp/card|backUp/py|backUp/utils/|backUp/test|jd_fruits.js|jd_pet.js|jd_factory.js|jd_health.js|jd_sgmh.js|jd_dreamFactory.js|jd_plantBean.js" "^(jd|JD|JS)[^_]|USER|sendNotify|utils"
```

青蛙https://t.me/s_guaguagua
部分需要进tg拿token
```sh
ql repo https://github.com/smiek2121/scripts.git "jd_|gua_" "" "ZooFaker_Necklace.js|JDJRValidator_Pure.js|sign_graphics_validate.js|cleancart_activity.js|jdCookie.js|sendNotify.js"
```

船长
使用教程：https://t.me/HarbourToulu/3052
【🛳船长库脚本汇总及变量🛳】
🛳 🛳jinggeng邀请入会有礼 (jd_jinggengInvite.py)
变量: export jinggengInviteJoin="活动&shopid"

🛳 🛳微定制组队通用脚本（jd_wdz.py）
变量: export jd_wdz_activityId="活动"

🛳 🛳邀好友赢大礼（jd_inviteFriendsGift.py）
变量: export jd_inv_authorCode="活动"

🛳 🛳一键领取店铺会员礼包（jd_shopCollectGift.py）
变量: export jd_shopCollectGiftId="活动"

🛳 🛳特效关注有礼 (jd_wxShopGift.py)
变量: export jd_wxShopGiftId="活动"

🛳 🛳生日礼包（jd_wxBirthGifts.py）
变量: export jd_wxBirthGiftsId="活动"

🛳 🛳完善信息有礼（jd_wxCompleteInfo.py）
变量: export jd_wxCompleteInfoId="活动&venderId"

🛳 🛳加购有礼（jd_wxCollectionActivity.py）
变量: export jd_wxCollectionActivityUrl="活动🔗" 
默认跑前10个账号，可自定义运行加购账号数量，变量：export jd_wxCollectionActivityRunNums="需要运行加购脚本的账号数量"

🛳 🛳通用开卡-shopLeague系列脚本（jd_shopLeague_opencard.py）
变量: export jd_shopLeagueId="活动"
并发变量: export jd_shopLeagueId_uuid=“你的助力码”

🛳 🛳通用开卡-joinCommon系列脚本（jd_joinCommon_opencard.py）
脚本变量: export jd_joinCommonId="活动&shopid"
并发变量: export jd_joinCommon_uuid=“你的助力码”

注：请先安装python依赖 redis、bs4两种依赖
docker-redis安装教程: 
①.先安装redis
复制以下命令到ssh一键安装
mkdir -p /mydata/redis/conf
touch /mydata/redis/conf/redis.conf
docker run -p 6379:6379 --name redis \
-v /mydata/redis/data:/data \
-v /mydata/redis/conf/redis.conf:/etc/redis/redis.conf \
-itd redis redis-server /etc/redis/redis.conf \
--appendonly yes
②.再青龙安装Python的redis依赖 （依赖管理 python3-->新建依赖-->redis）
redis环境变量(不填就是默认ip:port)：
export redis_url="redis服务器ip"  #填redis服务器ip
export redis_port="redis服务器端口"   #支持更换自定义端口
export redis_pwd=""  #没设置密码就空着

本地sign.so安装教程: 拉库, 运行HarbourJ库依赖一键安装脚本（jd_check_dependent.py）, 实现一键式全自动安装sign本地依赖文件；全自动报错也可去【 https://github.com/HarbourJ/HarbourToulu/releases 】下载架构与Py版本适配的文件解压放置 /青龙/scripts/HarbourJ_HarbourToulu_main文件夹内。
```sh
ql repo https://github.com/HarbourJ/HarbourToulu.git "jd_" "activity|backUp|jd_sign" "^jd[^_]|USER|utils|ZooFaker_Necklace|JDJRValidator_|sign_graphics_validate|jddj_cookie|function|ql|magic|JDJR|JD|sendNotify" "main"
```


#
- 傻妞一键安装
```
s=sillyGirl;a=arm64;if [[ $(uname -a | grep "x86_64") != "" ]];then a=amd64;fi ;if [ ! -d $s ];then mkdir $s;fi ;cd $s;wget http://gitee.yanyuge.workers.dev/https://github.com/cdle/${s}/releases/download/main/${s}_linux_$a -O $s && chmod 777 $s;pkill -9 $s;$(pwd)/$s
```
- 配置文件模板进`etc/sillyGirl`目录执行
```
wget https://gitee.com/yanyuwangluo/onekey/raw/master/sets.conf
```
- 傻妞docker版交互模式 ```docker attach sillygirl```
```
docker run \
    -itd \
    --name sillygirl \
    --restart always \
    -v  "$(pwd)"/sillyGirl:/etc/sillyGirl \
    mzzsfy/sillygirl:latest
```    
- 单独安装Maiark
- X86
```
wget -N --no-check-certificate https://github.com/1302557841/QL/raw/main/MaiARKx86 && chmod 777 MaiARKx86 && ./MaiARKx86
```
- 后台运行
```
nohup ./MaiARKx86 &
```
- Maiarkdocker版
```
 docker run -d \
    --name MaiARK \
    --hostname MaiARK \
    --restart=always \
    -v /opt/maiark:/MaiARK \
    -p 5701:8082 \
    kissyouhunter/maiark
```

- 单独安装rabbit一键脚本#一键更新#可用于部署和更新
- 国内机：
```sh
bash <(curl -s -L https://git.gushao.club/https://github.com/1302557841/QL/raw/main/RabbitUtils.sh)
```
- 国外鸡：
```sh
bash <(curl -s -L https://raw.githubusercontent.com/AyeSt0/MadRabbit_Utils/master/RabbitUtils.sh)
```
- Qrabbit：
```sh
bash <(curl -s -L https://git.gushao.club/https://raw.githubusercontent.com/AyeSt0/MadRabbit_Utils/master/QRabbitUtils.sh)
```

- 仓库地址：https://github.com/AyeSt0/MadRabbit_Utils

- 单独安装JDX
```sh
docker run -d --restart always -p 5705:80 -v /root/jdx/config:/jdx/config --name jdx aaron8/jdx
```

- 单独安装阿东一键脚本（免费有限制，一天扫码2次，低调使用，如有批量需求，请捐赠原作者）
```sh
bash -c "$(curl -fsSL https://git.gushao.club/https://raw.githubusercontent.com/1302557841/QL/main/adong/adong.sh)"
```

- 人形bot Docker 一键安装：
```sh
wget https://raw.githubusercontent.com/TeamPGM/PagerMaid-Pyro/development/utils/docker.sh -O docker.sh && chmod +x docker.sh && bash docker.sh
```
## 感谢！


> [`whyour`]
> [`danshui`]
> [`feverrun`]
> [`Aaron-lv`]
> [`faker2`] 
