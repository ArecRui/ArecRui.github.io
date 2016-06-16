
---

{% include toc %}

---


# Week 1 Why Program?

# 第一周

## 欢迎用Python

- Python的发明者Guido 介绍为什么要学习

## 1.1 为什么要编程

1. 人们发明电脑是为了让计算机为我们做事。如果我们不学习计算机的语言，我们就没法告诉计算机我们要做什么。编程就是学习计算机的语言，用计算机能懂的方式命令它按照我们的指令做事。

2. 用户 VS 程序员的区别：

<!--more-->
	- 用户把计算机当做一套工具，比如word，Excel，PPT等程序
	- 程序员理解计算机的方式和计算机的语言
	- 程序员拥有一些基础工具使他们能够构建给用户使用的工具
	- 程序员有时候编写一些大程序给很多人使用（比如浏览器），有时候只是一些小程序解决小问题（比如文件批量重命名工具）

3. 为什么要成为程序员

	- 解决自己的问题，比如我需要批量的删除一个问卷里面的某些不想要的字符
	- 解决他们的问题，比如制作一个网站后台管理系统，这就是程序员的工作了

4. 三个相关的概念

- 代码（Code）
	- 利用一段左右左右的舞蹈的指示来比如代码
	- 表达的失误来比喻bug
- 软件（Software）
- 程序（Program）
	- 比如计算在一个跳跃的段落中算出有多少个the，来表明什么时候需要用到程序

## 1.2 硬件基础

1. 几个定义
- 中央处理器（Central Processing Unit）：即CPU，俗称计算机的“大脑”，控制程序中指令执行的顺序，总是在问“what's next?"
- 输入设备（Input Devices）：如键盘、鼠标等
- 输出设备（Output Devices）：显示屏、麦克风、打印机等
- 主存储器（Main Memory）：即主存，相当于计算机的内存，存储容量小且是暂时性的，当机器电源关闭，存于其中的数据就会丢失。
- 辅助存储器（Secondary Memory）：即外存，相当于计算机的硬盘，存储容量大，断电后仍能保存数据，如硬盘、记忆棒等。.
2. 如图所示，程序员在主存那一块活动，将程序记录在主存，然后CPU执行程序中的指令。
3. 程序员将指令转换为Source Code（源代码，比如Pyhon），然后通过解释器转换为Machine Language（机器语言，二进制），这样计算机就可以理解程序员了。
4. 通过Totally Hot CPU这个视频讲解计算机在运行指令的时候，发热量是非常大的

## 1.3 Python作为一种编程语言

1. Python是Python解释器使用的编程语言，创始人是Guido van Rossum。
2. 语法错误（Syntax Errors）：刚开始学Python，很容易犯错，这是Python中的语法错误
3. 在Python的运行窗口中，主提示符“         ”其实就是在问你：what's next？
4. 老师通过随意输入一些代码，演示什么是语法错误，以及演示一个简单的四则运算，讲解什么是正确的语法
5. Python的构成元素
	- 就像一个故事一样，Python的代码要有开头、中间和结尾
	- 变量（Variables）
	- 常量（constant）
	- 运算器（operator）
	- 保留字（Reserved words）：保留字是指已经定义过的字，使用者不能再将这些字作为变量名，如if, while，not,try, else,while等。
	- 语句结构（Sentences/lines）：Assignment statement，assigment with expression，print statment
	- 故事结构（Story structure）：有目的地构建程序

## 1.4 撰写Python的段落

1. Python的脚本模型
	- 交互模式：一句一句地写指令，每句Python都会反应，一般用来演示
	- 脚本：大部分的程序都是有很长的段落的，通常会编成1个长的文档，然后在这个文档加上一个py的后缀，这样计算机就能识别出是python的程序
2. 程序流程（Program Flow）
	- 顺序执行（Sequential Steps）
	- 条件执行（Conditional Steps）：如if语句
	- 循环执行（Repeated Steps）：存在迭代变量（iteration variables）

## 1.5 An animated short python story

1. 解释程序其实就是把人的思想分解，比如在一个数字图表中，人是如何找出最大的数字的
2. 再次思考，计算机在下面的三个场景中如何找出最大的数字，有点像在解释算法的精神：
	- 第一个是全部显示，但是屏幕移动；
	- 第二个把数字颠倒；
	- 第三个逐个显示；
