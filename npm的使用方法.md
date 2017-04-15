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
npm config 的命令能够编辑和改写用户和全局的npmrc文件的内容。
