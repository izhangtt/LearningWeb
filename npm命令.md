# mac下nodejs 更新到最新版本的最新方法 
## 第一步：使用npm安装n模块
n模块是专门用来管理nodejs版本的
```
sudo npm install -g n
```
**提示**: 如果不使用sudo作为前缀，很可能出现权限访问异常导致安装失败

## 第二步：升级nodejs
升级nodejs是有两种方法： 
- 第一种是升级到最新版本
```
sudo n latest
```
- 第二种是升级到稳定版本
```
sudo n stable
```
**提示**: 建议是稳定版本 

# update npm:
sudo npm update npm -g

# angular安装：
1.全局安装 Angular CLI：npm install -g @angular/cli；
2.创建新项目
打开终端窗口。运行下列命令来生成一个新项目以及应用的骨架代码：
ng new my-app
3.步骤3. 启动开发服务器。进入项目目录，并启动服务器。
cd my-app
ng serve --open

# ionic安装：
1.sudo npm install -g ionic/sudo npm install -g cordova
2.$ ionic start cutePuppyPics
3.$ cd cutePuppyPics
4.$ ionic serve
//常见错误
Error: Cannot find module '@ionic/app-scripts'，解决：npm install @ionic/app-scripts@latest --save-dev；或npm i @ionic/app-scripts

# 设置npm的registry
```shell
方法一：
npm config set registry https://registry.npm.taobao.org -g
方法二：
npm install -g cnpm --registry=https://registry.npm.taobao.org
```
#  安装Vuew
## 全局安装 vue-cli
```
npm install --global vue-cli
```
## 创建一个基于 webpack 模板的新项目
```
vue init webpack my-project
```
## 安装依赖，走你
```
cd my-project
npm install
npm run dev
```
## 淘宝镜像
```
npm config set registry https://registry.npm.taobao.org
检查是否配置成功：npm config list
```
