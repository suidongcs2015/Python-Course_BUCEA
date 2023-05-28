# Part I. Python 发展历程
## 1. Python简史
### 1.1 Python的起源
Python的作者，Guido von Rossum，确实是荷兰人。1982年，Guido从阿姆斯特丹大学(University of Amsterdam)获得了数学和计算机硕士学位。然而，尽管他算得上是一位数学家，但他更加享受计算机带来的乐趣。用他的话说，尽管拥有数学和计算机双料资质，他总趋向于做计算机相关的工作，并热衷于做任何和编程相关的工作。

![image](https://github.com/suidongcs2015/Python-Course_BUCEA/assets/12708153/6b170c5c-4591-45fd-9011-1324dfe5c2d9)

1989年，为了打发圣诞节假期，Guido开始写Python语言的编译/解释器。Python来自Guido所挚爱的电视剧Monty Python's Flying Circus (BBC1960-1970年代播放的室内情景幽默剧，以当时的英国生活为素材)。他希望这个新的叫做Python的语言，能实现他的理念(一种C和shell之间，功能全面，易学易用，可拓展的语言)。Guido作为一个语言设计爱好者，已经有过设计语言的(不很成功)的尝试。这一次，也不过是一次纯粹的hacking行为。

### 1.2 Python的诞生

1991年，第一个Python编译器(同时也是解释器)诞生。它是用C语言实现的，并能够调用C库(.so文件)。从一出生，Python已经具有了：类(class)，函数(function)，异常处理(exception)，包括表(list)和词典(dictionary)在内的核心数据类型，以及模块(module)为基础的拓展系统。

![image](https://github.com/suidongcs2015/Python-Course_BUCEA/assets/12708153/be5a312f-bf8c-4971-8b81-c4afea1bb0a3)
最初的Python logo: 由Guido的兄弟Just von Rossum设计

Python语法很多来自C，但又受到ABC语言的强烈影响。来自ABC语言的一些规定直到今天还富有争议，比如强制缩进。但这些语法规定让Python容易读。另一方面，Python聪明的选择服从一些惯例(特别是C语言的惯例)。比如使用等号赋值，使用def来定义函数。Guido认为，如果“常识”上确立的东西，没有必要过度纠结。

Python从一开始就特别在意可拓展性(extensibility)。Python可以在多个层次上拓展。从高层上，你可以引入.py文件。在底层，你可以引用C语言的库。Python程序员可以快速的使用Python写.py文件作为拓展模块。但当性能是考虑的重要因素时，Python程序员可以深入底层，写C程序，编译为.so文件引入到Python中使用。Python就好像是使用钢构建房一样，先规定好大的框架。而程序员可以在此框架下相当自由的拓展或更改。

最初的Python完全由Guido本人开发。Python得到Guido同事的欢迎。他们迅速的反馈使用意见，并参与到Python的改进。Guido和一些同事构成Python的核心团队。他们将自己大部分的业余时间用于hack Python (也包括工作时间，因为他们将Python用于工作)。随后，Python拓展到CWI之外。Python将许多机器层面上的细节隐藏，交给编译器处理，并凸显出逻辑层面的编程思考。Python程序员可以花更多的时间用于思考程序的逻辑，而不是具体的实现细节 (Guido有一件T恤，写着：人生苦短，我用Python)。这一特征吸引了广大的程序员。Python开始流行。

我们不得不暂停我们的Python时间，转而看一看这时的计算机概况。1990年代初，个人计算机开始进入普通家庭。Intel发布了486处理器，windows发布window 3.0开始的一系列视窗系统。计算机的性能大大提高。程序员开始关注计算机的易用性  (比如图形化界面)。

![image](https://github.com/suidongcs2015/Python-Course_BUCEA/assets/12708153/6f0a2832-9bfe-4c32-8bc9-a9997c30dbae)
Windows3.0


由于计算机性能的提高，软件的世界也开始随之改变。硬件足以满足许多个人电脑的需要。硬件厂商甚至渴望高需求软件的出现，以带动硬件的更新换代。C++和Java相继流行。C++和Java提供了面向对象的编程范式，以及丰富的对象库。在牺牲了一定的性能的代价下，C++和Java大大提高了程序的产量。语言的易用性被提到一个新的高度。我们还记得，ABC失败的一个重要原因是硬件的性能限制。从这方面说，Python要比ABC幸运许多。

另一个悄然发生的改变是Internet。1990年代还是个人电脑的时代，windows和Intel挟PC以令天下，盛极一时。尽管Internet为主体的信息革命尚未到来，但许多程序员以及资深计算机用户已经在频繁使用Internet进行交流 (包括email和newsgroup)。Internet让信息交流成本大大下降。一种新的软件开发模式开始流行：开源 (open source)。程序员利用业余时间进行软件开发，并开放源代码。1991年，Linus在comp.os.minix新闻组上发布了Linux内核源代码，吸引大批hacker的加入。Linux和GNU相互合作，最终构成了一个充满活力的开源平台。

硬件性能不是瓶颈，Python又容易使用，所以许多人开始转向Python。Guido维护了一个maillist，Python用户就通过邮件进行交流。Python用户来自许多领域，有不同的背景，对Python也有不同的需求。Python相当的开放，又容易拓展，所以当用户不满足于现有功能，很容易对Python进行拓展或改造。随后，这些用户将改动发给Guido，并由Guido决定是否将新的特征加入到Python或者标准库中。如果代码能被纳入Python自身或者标准库，这将极大的荣誉。Python自身也因此变得更好。

(Guido不得不作出许多决定，这也是他被称为Benevolent Dictator For Life的原因)

Python被称为“Battery Included”，是说它以及其标准库的功能强大。这些是整个社区的贡献。Python的开发者来自不同领域，他们将不同领域的优点带给Python。比如Python标准库中的正则表达(regular expression)是参考Perl，而lambda, map, filter, reduce函数参考Lisp。Python本身的一些功能以及大部分的标准库来自于社区。Python的社区不断扩大，进而拥有了自己的newsgroup，网站(python.org)，以及基金 (Python Software Foundation)。从Python 2.0开始，Python也从maillist的开发方式，转为完全开源的开发方式。社区气氛已经形成，工作被整个社区分担，Python也获得了更加高速的发展。

(由于Guido享有绝对的仲裁权，所以在Python早期maillist的开发时代，不少爱好者相当担心Guido的生命。他们甚至作出假设：如果Guido挂了的话，Python会怎样。见If Guido was hit by a bus)

到今天，Python的框架已经确立。Python语言以对象为核心组织代码(Everything is object)，支持多种编程范式(multi-paradigm)，采用动态类型(dynamic typing)，自动进行内存回收(garbage collection)。Python支持解释运行(interpret)，并能调用C库进行拓展。Python有强大的标准库 (battery included)。由于标准库的体系已经稳定，所以Python的生态系统开始拓展到第三方包。这些包，如Django, web.py, wxpython, numpy, matplotlib,PIL，将Python升级成了物种丰富的热带雨林。

今天Python已经进入到3.0的时代。由于Python 3.0向后不兼容，所以从2.0到3.0的过渡并不容易。另一方面，Python的性能依然值得改进，Python的运算性能低于C++和Java(见Google的讨论)。Python依然是一个在发展中的语言。我期待看到Python的未来。

### 1.3 Python启示录
Python崇尚优美、清晰、简单，是一个优秀并广泛使用的语言 (TIOBE语言排行第八，Google的第三大开发语言，Dropbox的基础语言，豆瓣的服务器语言)。这个世界并不缺乏优秀的语言，但Python的发展史作为一个代表，带给我许多启示。

在Python的开发过程中，社区起到了重要的作用。Guido自认为自己不是全能型的程序员，所以他只负责制订框架。如果问题太复杂，他会选择绕过去，也就是cut the corner。这些问题最终由社区中的其他人解决。社区中的人才是异常丰富的，就连创建网站，筹集基金这样与开发稍远的事情，也有人乐意于处理。如今的项目开发越来越复杂，越来越庞大，合作以及开放的心态成为项目最终成功的关键。

Python从其他语言中学到了很多，无论是已经进入历史的ABC，还是依然在使用的C和Perl，以及许多没有列出的其他语言。可以说，Python的成功代表了它所有借鉴的语言的成功。同样，Ruby借鉴了Python，它的成功也代表了Python某些方面的成功。每个语言都是混合体，都有它优秀的地方，但也有各种各样的缺陷。同时，一个语言“好与不好”的评判，往往受制于平台、硬件、时代等等外部原因。程序员经历过许多语言之争。我想，为什么不以开放的心态和客观的分析，去区分一下每个语言的具体优点缺点，去区分内部和外部的因素。说不定哪一天发现，我不喜欢的某个语言中，正包含了我所需要的东西。

无论Python未来的命运如何，Python的历史已经是本很有趣的小说。

# Part II Python 特点与环境
## 2.1 Python的优缺点

Python的优点很多，简单的可以总结为以下几点。

1. 简单明了，学习曲线低，比很多编程语言都容易上手。
2. 开放源代码，拥有强大的社区和生态圈，尤其是在数据分析和机器学习领域。
3. 解释型语言，天生具有平台可移植性，代码可以工作于不同的操作系统。
4. 对两种主流的编程范式（面向对象编程和函数式编程）都提供了支持。
5. 代码规范程度高，可读性强，适合有代码洁癖和强迫症的人群。

Python的缺点主要集中在以下几点。

1. 执行效率稍低，对执行效率要求高的部分可以由其他语言（如：C、C++）编写。
2. 代码无法加密，但是现在很多公司都不销售卖软件而是销售服务，这个问题会被弱化。
3. 在开发时可以选择的框架太多（如Web框架就有100多个），有选择的地方就有错误。

## 2.2 Python的应用领域

目前Python在Web应用后端开发、云基础设施建设、DevOps、网络数据采集（爬虫）、自动化测试、数据分析、机器学习等领域都有着广泛的应用。

## 2.3 安装Python解释器

想要开始Python编程之旅，首先得在自己使用的计算机上安装Python解释器环境，下面将以安装官方的Python解释器为例，讲解如何在不同的操作系统上安装Python环境。官方的Python解释器是用C语言实现的，也是使用最为广泛的Python解释器，通常称之为CPython。除此之外，Python解释器还有Java语言实现的Jython、C#语言实现的IronPython以及PyPy、Brython、Pyston等版本，有兴趣的读者可以自行了解。

## 2.4 Windows环境

可以在[Python官方网站](https://www.python.org)下载到Python的Windows安装程序（exe文件），需要注意的是如果在Windows 7环境下安装Python 3.x，需要先安装Service Pack 1补丁包（可以通过一些工具软件自动安装系统补丁的功能来安装），安装过程建议勾选“Add Python 3.x to PATH”（将Python 3.x添加到PATH环境变量）并选择自定义安装，在设置“Optional Features”界面最好将“pip”、“tcl/tk”、“Python test suite”等项全部勾选上。强烈建议选择自定义的安装路径并保证路径中没有中文。安装完成会看到“Setup was successful”的提示。如果稍后运行Python程序时，出现因为缺失一些动态链接库文件而导致Python解释器无法工作的问题，可以按照下面的方法加以解决。

如果系统显示api-ms-win-crt\*.dll文件缺失，可以参照[《api-ms-win-crt\*.dll缺失原因分析和解决方法》](<https://zhuanlan.zhihu.com/p/32087135>)一文讲解的方法进行处理或者直接在[微软官网](https://www.microsoft.com/zh-cn/download/details.aspx?id=48145)下载Visual C++ Redistributable for Visual Studio 2015文件进行修复；如果是因为更新Windows的DirectX之后导致某些动态链接库文件缺失问题，可以下载一个[DirectX修复工具](<https://dl.pconline.com.cn/download/360074-1.html>)进行修复。

## 2.5 Linux环境

Linux环境自带了Python 2.x版本，但是如果要更新到3.x的版本，可以在[Python的官方网站](https://www.python.org)下载Python的源代码并通过源代码构建安装的方式进行安装，具体的步骤如下所示（以CentOS为例）。

1. 安装依赖库（因为没有这些依赖库可能在源代码构件安装时因为缺失底层依赖库而失败）。

```Shell
yum -y install wget gcc zlib-devel bzip2-devel openssl-devel ncurses-devel sqlite-devel readline-devel tk-devel gdbm-devel db4-devel libpcap-devel xz-devel libffi-devel
```

2. 下载Python源代码并解压缩到指定目录。

```Shell
wget https://www.python.org/ftp/python/3.7.6/Python-3.7.6.tar.xz
xz -d Python-3.7.6.tar.xz
tar -xvf Python-3.7.6.tar
```

3. 切换至Python源代码目录并执行下面的命令进行配置和安装。

```Shell
cd Python-3.7.6
./configure --prefix=/usr/local/python37 --enable-optimizations
make && make install
```

4. 修改用户主目录下名为.bash_profile的文件，配置PATH环境变量并使其生效。

```Shell
cd ~
vim .bash_profile
```

```Shell
# ... 此处省略上面的代码 ...

export PATH=$PATH:/usr/local/python37/bin

# ... 此处省略下面的代码 ...
```

5. 激活环境变量。

```Shell
source .bash_profile
```

## 2.6 macOS环境

macOS也自带了Python 2.x版本，可以通过[Python的官方网站](https://www.python.org)提供的安装文件（pkg文件）安装Python 3.x的版本。默认安装完成后，可以通过在终端执行`python`命令来启动2.x版本的Python解释器，启动3.x版本的Python解释器需要执行`python3`命令。

### 运行Python程序

#### 确认Python的版本

可以Windows的命令行提示符中键入下面的命令。

```Shell
python --version
```
在Linux或macOS系统的终端中键入下面的命令。

```Shell
python3 --version
```

当然也可以先输入`python`或`python3`进入交互式环境，再执行以下的代码检查Python的版本。

```Python
import sys

print(sys.version_info)
print(sys.version)
```

# Part III Python 代码特点
## 3.1 编写Python源代码

可以用文本编辑工具（推荐使用[Sublime](<https://www.sublimetext.com/>)、[Visual Studio Code](<https://code.visualstudio.com/>)等高级文本编辑工具）编写Python源代码并用py作为后缀名保存该文件，代码内容如下所示。

```Python
print('hello, world!')
```

## 3.2 运行程序

切换到源代码所在的目录并执行下面的命令，看看屏幕上是否输出了"hello, world!"。

```Shell
python hello.py
```

或

```Shell
python3 hello.py
```

## 3.3 代码中的注释

注释是编程语言的一个重要组成部分，用于在源代码中解释代码的作用从而增强程序的可读性和可维护性，当然也可以将源代码中不需要参与运行的代码段通过注释来去掉，这一点在调试程序的时候经常用到。注释在随源代码进入预处理器或编译时会被移除，不会在目标代码中保留也不会影响程序的执行结果。

1. 单行注释 - 以#和空格开头的部分
2. 多行注释 - 三个引号开头，三个引号结尾

```Python
"""
第一个Python程序 - hello, world!
向伟大的Dennis M. Ritchie先生致敬

Version: 0.1
Author: *******
"""
print('hello, world!')
# print("你好, 世界！")
```

# Part IV Python开发工具

## 4.1 IDLE - 自带的集成开发工具
![image](https://github.com/suidongcs2015/Python-Course_BUCEA/assets/12708153/22863316-3eb2-4f6c-95f2-37262f270d17)

IDLE是安装Python环境时自带的集成开发工具，如下图所示。但是由于IDLE的用户体验并不是那么好所以很少在实际开发中被采用。


## 4.2 IPython - 更好的交互式编程工具

IPython是一种基于Python的交互式解释器。相较于原生的Python交互式环境，IPython提供了更为强大的编辑和交互功能。可以通过Python的包管理工具pip安装IPython，具体的操作如下所示。

```Shell
pip install ipython
```

或

```Shell
pip3 install ipython
```

安装成功后，可以通过下面的ipython命令启动IPython，如下图所示。

![image](https://github.com/suidongcs2015/Python-Course_BUCEA/assets/12708153/60494d25-e0a3-4d92-b784-84ea0ebfcba4)

## 4.3 Sublime Text - 高级文本编辑器

![image](https://github.com/suidongcs2015/Python-Course_BUCEA/assets/12708153/3e897841-517e-4010-8ed2-a4403352e834)

- 首先可以通过[官方网站](https://www.sublimetext.com/)下载安装程序安装Sublime Text 3或Sublime Text 2。

- 安装包管理工具。
  1. 通过快捷键Ctrl+`或者在View菜单中选择Show Console打开控制台，输入下面的代码。

  - Sublime 3

  ```Python
  import  urllib.request,os;pf='Package Control.sublime-package';ipp=sublime.installed_packages_path();urllib.request.install_opener(urllib.request.build_opener(urllib.request.ProxyHandler()));open(os.path.join(ipp,pf),'wb').write(urllib.request.urlopen('http://sublime.wbond.net/'+pf.replace(' ','%20')).read())
  ```
  - Sublime 2

  ```Python
  import  urllib2,os;pf='Package Control.sublime-package';ipp=sublime.installed_packages_path();os.makedirs(ipp)ifnotos.path.exists(ipp)elseNone;urllib2.install_opener(urllib2.build_opener(urllib2.ProxyHandler()));open(os.path.join(ipp,pf),'wb').write(urllib2.urlopen('http://sublime.wbond.net/'+pf.replace(' ','%20')).read());print('Please restart Sublime Text to finish installation')
  ```
  2. 在浏览器中输入  https://sublime.wbond.net/Package%20Control.sublime-package 下载包管理工具的安装包，并找到安装Sublime目录下名为&quot;Installed Packages&quot;的目录，把刚才下载的文件放到这个文件加下，然后重启Sublime Text就搞定了。


- 安装插件。通过Preference菜单的Package Control或快捷键Ctrl+Shift+P打开命令面板，在面板中输入Install Package就可以找到安装插件的工具，然后再查找需要的插件。我们推荐大家安装以下几个插件：

  - SublimeCodeIntel - 代码自动补全工具插件。
  - Emmet - 前端开发代码模板插件。
  - Git - 版本控制工具插件。
  - Python PEP8 Autoformat - PEP8规范自动格式化插件。
  - ConvertToUTF8 - 将本地编码转换为UTF-8。

> **说明**：事实上[Visual Studio Code](<https://code.visualstudio.com/>)可能是更好的选择，它不用花钱并提供了更为完整和强大的功能，有兴趣的读者可以自行研究。

## 4.4  PyCharm - Python开发神器

PyCharm的安装、配置和使用在[《玩转PyCharm》](../番外篇/玩转PyCharm.md)进行了介绍，有兴趣的读者可以选择阅读。

![image](https://github.com/suidongcs2015/Python-Course_BUCEA/assets/12708153/b75d5419-8817-41dd-868d-064c811f697b)

## 4.5  练习

1. 在Python交互式环境中输入下面的代码并查看结果，请尝试将看到的内容翻译成中文。

    ```Python
    import this
    ```

    > **说明**：输入上面的代码，在Python的交互式环境中可以看到Tim Peter撰写的[“Python之禅”](../Python之禅.md)，里面讲述的道理不仅仅适用于Python，也适用于其他编程语言。

2. 学习使用turtle在屏幕上绘制图形。

    > **说明**：turtle是Python内置的一个非常有趣的模块，特别适合对计算机程序设计进行初体验的小伙伴，它最早是Logo语言的一部分，Logo语言是Wally Feurzig和Seymour Papert在1966发明的编程语言。

    ```Python
    import turtle
    
    turtle.pensize(4)
    turtle.pencolor('red')
    
    turtle.forward(100)
    turtle.right(90)
    turtle.forward(100)
    turtle.right(90)
    turtle.forward(100)
    turtle.right(90)
    turtle.forward(100)
    
    turtle.mainloop()
    ```
