### npm的常见命令  
#### 1. npm init  
npm init 是为了生成一个package.json的文件，这个文件主要定义了这个项目所需要的各种模块，以及项目的配置信息（比如名称、版本、许可证等元数据）。npm install命令根据这个配置文件，自动下载所需的模块，也就是配置项目所需的运行和开发环境。  
``` js
{
  "name": "yuyanfang",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC"
}
```
#### 2. npm config
npm config 的命令能够编辑和改写用户和全局的npmrc文件的内容。npm config有很多子命令如下:
#### (1) set 设置配置
```
npm config set key value
```
如果value省略则默认为ture
#### (2)get 获取配置
```
npm config get key 
```
输出到标准输出
#### (3)list 获取全部的配置
```
npm config list
```
#### (4)delete 删除配置
```
npm config delete key
```
#### (5)edit 获取全部的配置
```
npm config edit 
```
会打开配置文件进行修改。
#### 3. npm info 
npm info后面加模块名称，可以该模块的信息
#### 4. npm list
npm list 可以查看该项目安装的所有模块，以及它们依赖的模块。
#### 5.npm install
Node模块采用npm install命令安装。
每个模块可以“全局安装”，也可以“本地安装”。“全局安装”指的是将一个模块安装到系统目录中，各个项目都可以调用。一般来说，全局安装只适用于工具模块，比如eslint和gulp。“本地安装”指的是将一个模块下载到当前项目的node_modules子目录，然后只有在项目目录之中，才能调用这个模块。
#### （1）本地安装
```node
npm install <package name>/git://github.com/package/path.git
```
#### （2）全局安装 -g / -global
```node
npm install -g <package name>/ git://github.com/package/path.git
npm install -global <package name>/ git://github.com/package/path.git
```
#### （3）强制安装 -f / --force
安装之前，npm install会先检查，node_modules目录之中是否已经存在指定模块。如果存在，就不再重新安装了，即使远程仓库已经有了一个新版本，也是如此。
如果你希望，一个模块不管是否安装过，npm 都要强制重新安装，可以使用**-f**或**--force**参数。
```node
npm install -g <package name>/ git://github.com/package/path.git -f
npm install -global <package name>/ git://github.com/package/path.git --force
```
#### （4）安装不同版本 @版本号 @lastest
```node
npm install [<@scope>/] <package name>@<version>
npm install [<@scope>/] <package name>@<version range>
npm install [<@scope>/] <package name>@lastest
#安装最新的本版本的包
```
#### (5)共同的option
> –save：模块名将被添加到dependencies，可以简化为参数-S。
> –save-dev: 模块名将被添加到devDependencies，可以简化为参数-D。
```
npm install [<@scope>/] <package name>--save
npm install [<@scope>/] <package name> --save-dev
#或者
npm install [<@scope>/] <package name> -S
npm install [<@scope>/] <package name> -D
```








