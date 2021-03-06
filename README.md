安装git
安装nvm
nvm install 8.11.1
nvm use 8.11.1
安装mongo
git clone https://github.com/princeljf/DOClever.git

docker安装mongo
https://www.runoob.com/docker/docker-install-mongodb.html
docker pull mongo:latest
docker run -itd --name mongo -p 27017:27017 mongo

npm run start

－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－

1.首先本地要安装node环境，推荐8.11.1版本(下载页面)
2.安装mongodb(下载页面)
https://www.mongodb.com/
可使用robomongo来作为mongodb的客户端工具(下载页面)
https://robomongo.org/
启动mongodb后（如何启动）
https://www.open-open.com/lib/view/open1435117403544.html
用robomongo来连接，新建一个database作为DOClever的数据库（名称随意）
源码部署
将DOClever的源码down到本地，在命令行下运行node DOClever的根目录/Server/bin/www（如果是windows环境下，请修改目录分隔符)，第一次启动，会出现命令行提示符，按照提示符输入即可完成相关的配置，等到DOClever启动成功后， 在浏览器里输入localhost:DOClever启动的端口号,出现首页表示部署成功。
npm部署
在命令行下运行npm install doclever -g，等doclever包安装成功后，运行doclever进行第一次配置（如果有问题，就运行doclever --installwithsetup）


－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－－


## 什么是DOClever？
DOClever是一个商业化开源产品，完全免费。无论你是前端工程师，还是后端工程师，接口永远都是两者交互的桥梁，所以DOClever专为中小型团队量身打造，旨在解决接口的管理，测试与数据生成，实现真正的一体化解决方案。
## DOClever接下来的开发计划
4.13
重制版发布（server端，网页端，桌面端重构完成，包括bug fix，前端UI共用一套，前端路由，重写导出功能，完善多语言，添加日志系统，实现缓存桥接）

4.20
支持接口鉴权
添加类似postman快速测试的功能
开放接口，项目和团队的对外api

5.1
支持websocket测试 ,支持webservice测试
添加数据库支持，可以测试sql语句，可以匹配接口结果
开放测试，文档的对外api

5.10 
重构自动化测试功能

5.20
在桌面端添加分布式压力测试

6.1
开发微信服务号功能
## DOClever有哪些功能
1.可以对接口信息进行编辑管理，支持get,post,put,delete,patch五种方法，支持http和https协议，并且支持query，body，json，raw，rest，formdata的参数可视化编辑。同时对json可以进行无限层次可视化编辑。并且，状态码，代码注入，markdown文档等附加功能应有尽有。

2.接口调试运行，一个都不能少，可以对参数进行加密，从md5到aes一应俱全，返回参数与模型实时分析对比，给出不一致的地方，找出接口可能出现的问题。如果你不想手写文档，那么试试接口的数据生成功能，可以对接口运行的数据一键生成文档信息。

3.mock的无缝整合，DOClever自己就是一个mock服务器，当你把接口的开发状态设置成已完成，本地mock便会自动请求真实接口数据，否则返回事先定义好的mock数据。

4.支持postman，rap，swagger的导入，方便你做无缝迁移，同时也支持html文件的导出，方便你离线浏览！

5.项目版本和接口快照功能并行，你可以为一个项目定义1.0，1.1，1.2版本，并且可以自由的在不同版本间切换回滚，再也不怕接口信息的遗失，同时接口也有快照功能，当你接口开发到一半或者接口需求变更的时候，可以随时查看之前编辑的接口信息。

6.自动化测试功能，目前市面上类似平台的接口自动化测试大部分都是伪自动化，对于一个复杂的场景，比如获取验证码，登陆，获取订单列表，获取某个特定订单详情这样一个上下文关联的一系列操作无能为力。而DOClever独创的自动化测试功能，只需要你编写极少量的javascript代码便可以在网页里完成这样一系列操作，同时，DOClever还提供了后台定时批量执行测试用例并把结果发送到团队成员邮箱的功能，你可以及时获取接口的运行状态。

7.团队协作功能，很多类似的平台这样的功能是收费的，但是DOClever觉得好东西需要共享出来，你可以新建一个团队，并且把团队内的成员都拉进来，给他们分组，给他们分配相关的项目以及权限，发布团队公告等等。

8.DOClever开源免费，支持内网部署，很多公司考虑到数据的安全性，不愿意把接口放到公网上，没有关系，DOClever给出一个方便快捷的解决方案，你可以把平台放到自己的内网上，完全不需要连接外网，同时功能一样也不少，即便是对于产品的升级，DOClever也提供了很便捷的升级方案！
## 产品文档
http://doclever.cn
## DOClever开源
本次开源的是DOClever的内网版本，可以直接部署到内网中，和线上版本在功能上是完全一样的，区别在于：

1.线上的系统用了前端和后端两套工程，并且用nginx做了负载均衡，redis做缓存，而内网版本合并为一个工程，直接用node做静态服务器，取消了缓存，这样对于很多中小型团队来说很轻便而且也够用了。

2.线上系统在安全性方面做了不少加固处理，而内网版本默认内网是安全的，也为了提高node作为服务器的效率，取消了很多加固处理，如果用户有需要可以自行添加。

3.开源版本去掉了线上的宣传和介绍页面，只留下最精简的功能页面。
## 源码结构
Server为服务端，Client为网页端，Desktop为桌面端（编译桌面端需要安装electron相关npm包)
## 如何部署
1.首先本地要安装node环境，推荐8.11.1版本([下载页面](https://nodejs.org/en/))

2.安装mongodb([下载页面](https://www.mongodb.com/))，可使用robomongo来作为mongodb的客户端工具([下载页面](https://robomongo.org/))，启动mongodb后（[如何启动](http://www.open-open.com/lib/view/open1435117403544.html)），用robomongo来连接，新建一个database作为DOClever的数据库（名称随意）

### 源码部署
将DOClever的源码down到本地，在命令行下运行node DOClever的根目录/Server/bin/www（如果是windows环境下，请修改目录分隔符)，第一次启动，会出现命令行提示符，按照提示符输入即可完成相关的配置，等到DOClever启动成功后， 在浏览器里输入localhost:DOClever启动的端口号,出现首页表示部署成功。
### npm部署
在命令行下运行npm install doclever -g，等doclever包安装成功后，运行doclever进行第一次配置（如果有问题，就运行doclever --installwithsetup）
## 问题反馈
如果你有任何问题和建议，请在issues里面指出，每个月的1号和15号会发布功能迭代版本，根据bug情况不定期的会发布bug迭代版本。如果你想加入开源的大家庭，欢迎加入qq群：611940610
## 注意
本系统已申请专利著作权，请不要私自用于商业用途，如有发现，我们将保留对你的法律责任追究！
