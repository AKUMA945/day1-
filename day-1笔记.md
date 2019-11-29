一 npm(node package)node管理器

npm -v 查看版本号

内置模块  http fs url
需下包  bodyparser  express

二 npm管理包有哪些方面

1）本地下载

    安装本地开发依赖   ————>devDependencies字段内
    npm i <包名> --save-dev/-D
    
    
    
    安装本地线上依赖 ———>dependencies字段内
    npm i <包名> --save/-S

2）全局下载
    npm i <包名> -g

三 生成package.json

npm init
快速生成  npm init -y

  "name": "lianxi",      包名
  
  "version": "1.0.0",    版本号
  
  "description": "",     描述
  
  "main": "index.js",    入口文件
  
  "scripts": {           命令
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  
  "author": "",          作者
  
  "license": "ISC"
  
  
  四 nodejs ————>commonjs规范（1个js就是一个模块）
  抛出模块  module.exports / exports
  
  区别：exports是module.exports的别名
  
  module.exports:后者会覆盖前者
  
  exports：以属性的形式添加，不能直接赋值
  
  
  引入模块  require()
  
  五 npm包管理规则
  
  1)路径 ： 1 相对路径./
          2 绝对路径 /
          
  2)包名 
  第一步：node_modules文件的查找规则
  
  先从当前文件夹下面找————>一层一层向上找直到磁盘根目录————>全局配置环境变量NODE_PATH查找
  
  第二步：
  
  先对应包名文件夹————>package.json main字段 没有————>index.js
  
  六 npm root -g 查看全局下载包的路径
  
 报错 不是内外部命令，解决方法  找执行文件所在的目录配置到全局环境变量的path下
 
 
 七 设置镜像源 ：
 
 国外：http://registry.npmjs.org/
 
 淘宝：http://registry.npm.taobao.org
 
 npm config set registry <镜像地址> 设置镜像源地址
 
 npm config get registry 查看镜像源地址
 
 
 八 git生成公钥和秘钥  ssh-keygen
 
 https ： 每次提交代码 都需要输入用户名和密码
 
 ssh：配置公钥和秘钥
 
 九 npm常用命令
 
 npm view <包名> versions 所有版本
 
 npm view <包名> version  最新版本
 
 npm search <包名> 
 
 十 发包
 
 1. npm镜像源必须是国外的
 2. 必须要有packag.json文件
 3. 新建入口文件 编写功能
 4. npm login
 5. npm publish
 6. npm unpublish <包名> --force 24小时内可删除

 