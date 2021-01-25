## 命令行
### dir 列出当前目录下的所有文件
### cd 目录名 进入到指定的目录
### Desktop 桌面
### md 目录名 创建一个文件夹
### rd 目录名 删除一个文件夹
### . 表示当前目录
### .. 表示上一级目录
## 线程与进程
### 线程 计算机中的最小的计算单位，负责执行进程中的程序(相当于工厂中的工人)
### 进程 负责为程序的运行提供必备的环境(相当于工厂中的车间)
## 单线程
### js
## 多线程
### 大部分语言
## node版本
### 奇数版为开发版
### 偶数版为稳定版
## 模块化
### 在Node中，一个js文件就是一个模块
### 在Node中，每一个js文件中的js代码都是独立运行在一个函数中，而不是全局作用域，所以一个模块的变量和函数在其他模块中无法访问
## 暴露属性或方法
### exports.属性(方法)
## 模块标识
### 核心模块：由node提供，模块标识为模块名
### 文件模块：由用户自己创建模块，模块标识为文件路径(一般为相对路径)
### 每个模块的顶层隐藏函数：function (exports, require, module, _filename, _dirname) {}
### 顶层隐藏函数的五个实参：exports暴露/导出，require引入，module模块本身，_filename 当前模块的完整路径，_dirname当前模块所在文件夹的完整路径  
### exports和module.exports:exports只能通过使用.的方式来向外暴露内部对象，exports.xxx = xxxx;而module.exports既可以通过.的形式，也可以通过直接赋值，module.exports.xxx = xxxx,module.exports = {}
## 包结构
### package.json:描述文件(必需)
### bin 可执行二进制文件
### lib js代码
### doc 文档
### test 单元测试
## NPM
### Node包管理工具：Node Package Manager
### npm命令
#### npm -v 查看npm的版本
#### npm version 查看所有模块的版本
#### npm search 包名 搜索包
#### npm install / i 包名 安装包
#### npm remove / r 包名 删除包
#### npm install 包名 --save 安装包并添加到依赖
#### npm install 下载当前项目所依赖的包
#### npm install 包名 -g 全局安装包
## Buffer
### 缓冲区：存储二进制的文件
### buffer构建函数全部不推荐使用
### Buffer.from(str)将一个字符串转换为buffer
### Buffer.alloc(size)创建一个指定大小的Buffer
### Buffer.alloUnsafe(size)创建一个指定大小的Buffer，但是可能包含敏感数据
## node操作文件打开状态
### r 读取文件，文件不存在则出现异常
### r+ 读写文件，文件不存在则出现异常
### rs 在同步模式下打开文件用于读取
### rs+ 在同步模式下打开文件用于读写
### w 打开文件用于写操作，如果不存在则创建，如果存在则截断
### wx 打开文件用于写操作，如果存在则打开失败
### w+ 打开文件用于读写，如果不存在则创建，如果存在则截断
### wx+ 打开文件用于读写，如果存在则打开失败
### a 打开文件用于追加，如果路径存在则失败
### ax 打开文件用于追加，如果路径存在则失败
### a+ 打开文件进行读取和追加，如果不存在则创建该文件
### ax+ 打开文件进行读取和追加，如果路径存在则失败
### 需要记住(r 只读，w 可写，a 追加)
