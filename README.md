# installvue
###安装最新的nodejs,winows覆盖安装，苹果直接打命令，
完事配置环境变量，系统变量，npm缓存地址

***

>* 很多环境现在需要依赖node等环境,在构件vue项目的时候需要最新的node,[官网](https://nodejs.org/en/)下载最新安装包，自带npm最新版
>* mac 可以用n模块，首先安装n模块一行命令搞定

```
npm install -g n
n stable
```
* win系统就需要重现下载安装最新node
* 启动cmd,先配置npm的全局模块的存放路径以及cache的路径
```
npm config set prefix "C:\Program Files\nodejs\node_global"
npm config set cache "C:\Program Files\nodejs\node_cache"
```
<img src="https://github.com/yangjingjing1234/installvue/blob/master/Image.png">

* 配置node的环境变量,进入我的电脑→属性→高级→环境变量。
* 执行完node安装包之后，将node.exe所在的目录复制，加入系统环境变量PATH中，便于在任意位置执行node应用
* 在系统变量下新建"NODE_PATH"，输入”C:\Program Files\nodejs\node_global\node_modules“。这个目录一般都是node默认安装的路径，如果不是，自己找到相应的位置换掉
* 由于改变了module的默认地址，所以上面的用户变量都要跟着改变一下,用户变量找到path添加;%NODE_PATH%;
* 至此一些配置已经完成

***

#安装vue相关

安装webpack
```
npm install webpack -g
```
安装vue脚手架
```
npm install vue-cli -g
```

创建一个 webpack 项目并且下载依赖
##注意：后3个一定要为no  不然你会看到莫名其妙的校验错误，几乎寸步难行
<img src="https://github.com/yangjingjing1234/installvue/blob/master/Image1.png">
```
vue init webpack vue-name
```
##如果你的电脑已经有很多个vue项目以上的全局安装就不需要了，直接从创建目录开始
进入vue-name 目录
```
npm install 
```

启动服务(http://localhost:8080)

```
npm run dev
```
发布代码

```
npm run build
```