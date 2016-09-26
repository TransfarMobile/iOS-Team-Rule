# iOS架构

## 目录

* [代码规范](#style_guide)
* [项目架构(MVC)](#project_architecture)
* [工具](#tools)


<a name="style_guide"></a>
## 代码规范

###  [Objective-C](https://github.com/TransfarMobile/Objective-C-Style-Guide/blob/master/objective-c-style-guide-zh.md)

##常见业务规范
开发中出现的常见业务场景的处理方式，我们从更好的封装性，可读性，扩展性，和更高的开发效率出发，来做一些规范。  

###属性变量
除非在init方法中，否则永远使用getter方法来初始化属性变量。
###自定义UITableViewCell
1. 不要把新的自定义UITableViewCell的代码写在其他的文件中，使用新建文件的方式，来创建你的自定义UITableViewCell。

2. Cell的属性定义为私有属性，公有属性场景很少，如果真的有，先检查下你的设计是否需要改进。
3. Cell属性的定义和初始化等方式，依然遵循上文中的代码规范。

4. 给Cell声明一个公开的方法用来配置Cell的内容，而不是直接调用Cell的属性，在外面配置。
5. Cell的SubView的action target应该是Cell本身。将所有的action response直接写在Cell的内
部。

6. 用delegate的方式把事件回调出去，通常一个delegate方法即可，使用枚举来区分event类型。不要使用block来回调，这样会造成cellForRowAtIndex里面灾难性的代码堆砌，更不利用调试。



<a name="project_architecture"></a>
## 项目架构
###网络层
###登录系统
###本地存储
###第三方库 (json to model 网络状态UI)

<a name="tools"></a>
## 工具

### 1. Git

#### 1. Git学习：
* 教程：http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000

* 进阶教程：http://git-scm.com/book/zh/v1

* git及相关gui工具下载地址：http://git-scm.com/

#### 2. Git Team

* 写出好的 commit message
https://ruby-china.org/topics/15737

* Git分支管理是一门艺术
http://roclinux.cn/?p=2129

