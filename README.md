# lixing-mgt
nodeJs+koa+angularJs+bootStrap+mysql
一、代码管理
1、在GitHub上创建项目名称为【lixing-mgt】；
2、通过clone https://github.com/llsbdx/lixing-mgt.git 克隆项目到工作区;
3、添加项目说明，并通过git status查询变更文件；
4、通过git add 文件名 添加变更文件到暂存区；
5、通过git commit 文件名 提交文件到版本库；
6、通过git remote add origin https://github.com/llsbdx/lixing-mgt.git
       git push -u orgin master
   提交到远程仓库；
7、创建并切换到分支 git checkout -b dev
8、现在可以在分支上开发了。。。

二、搭建NodeJs环境
1、通过npm init 创建一个空目录（除package.json）
2、添加以下目录
   --models：存放操作数据库的文件
   --public：存放静态文件，如样式、图片等
     --css
     --img
   --routes：存放路由文件
   --views：存放模板文件
3、安装依赖模块
   通过npm i config-lite connect-flash connect-mongo ejs express express-formidable express-session marked moment sequelize  mysql objectid-to-timestamp sha1 winston express-winston --save 安装依赖包
   --express:web框架
   --express-session:session中间件
   --connect-flash:页面通知提示的中间件，基于session实现
   --ejs:模板
   --exptess-formidable:接收表单及文件上传中间件
   --config-lite:读取配置文件文件
   --marked:markdown解析
   --monent:时间格式
   --object-to-timestamp:根据ObjectId生成时间戳
   --sha1:sha1加密，密于密码加密
   --wiston:日志
   --express-winston:基于wiston的用于express的日志中间件
   --mysql:mysql驱动
   --sequelize:orm把关系数据库表结构映射到对象上

   注：
    npm i express --save / npm i express -S  (安装 express，同时将  "express": "^4.14.0"  写入 dependencies )

     npm i express --save-dev / npm i express -D  (安装 express，同时将  "express": "^4.14.0"  写入 devDependencies )
      npm i express --save --save-exact  (安装 express，同时将  "express": "4.14.0"  写入 dependencies 

4、锁定项目依赖包
   通过npm shrinkwrap 会生成npm-shrinkwrap.json文件，只要目录下有 npm-shrinkwrap.json 则运行  npm install  的时候会优先使用 npm-shrinkwrap.json 进行安装，没有则使用 package.json 进行安装。
三、将开发分支的变动合并到主干
1、通过git checkout master切换到主干；
2、通过git merge dev 将分支的变动合并到主干；
3、通过git branch -d dev 删除分支; 
4、通过git branch 查看分支
