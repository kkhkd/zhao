# 太子党关系网络
基于 编程随想 整理的《太子党关系网络》，专门揭露赵国的权贵。[zhao-visualized.netlify.app](https://zhao-visualized.netlify.app)可以看到这些人的关系。

我Fork了这个项目希望可以继续维护，同时也为了给我的数据可视化项目[《太子党关系网络》可交互视觉化](https://github.com/LuoSheng12345/zhao-visualized) 提供更新更准的数据。[来这里](https://github.com/LuoSheng12345/zhao/blob/master/OLD_README.wiki) 可以看到编程随想曾经写的README.wiki，编程随想的原repo [在这里](https://github.com/programthink/zhao)

## 如何为这个项目做贡献
如果你发现这个数据库的数据有问题，比如说数据错误、缺失、或者过时，希望可以修改、添加文件的话，可以通过以下的方式做贡献。

方法1：去https://github.com/LuoSheng12345/zhao/issues 那里开一个新的issue。我会根据你的issue进行手动更新。

方法2：直接点击你想要改的文件进行修改，并请求Pull Request。

方法3：如果要进行一些复杂的操作，可能需要使用git，把这个项目clone了之后创造新的branch，然后再pull request。

方法4：给我发个电子邮件，说明问题，我会根据你的反馈更新。我的电子邮件[luosheng12345abcde@gmail.com](mailto:luosheng12345abcde@gmail.com)

方法1-3需要GitHub账号，方法4不需要。不管使用那种方式都请提供一定的参考文献。

## 以下为编程随想所写的原来的README的内容

= 俺整理的《太子党关系网络》 =

== 简介 ==

此项目创建于2016年2月，专门用来揭露天朝的权贵（也就是传说中的“赵家人”）。

俺把这几年收集整理的数据开源到 GitHub，便于多人协作——大伙儿群策群力，一起来曝光权贵家族。

初次上传的数据包括：700多个数据文件（ '''对应700多人，130多个家族''' ），另有200多张图片（人物头像）。随着俺不断完善，数据会越来越多。

对这个项目，俺会【持续更新】。比如朝廷每次换届的时候，俺都会补充新的素材。

为了确保数据的可信度，俺主要参考“维基百科”以及一些国际权威媒体的报道（比如《纽约时报》、《华尔街日版》、《金融时报》等等）。

另外，对于某些客观事实（比如：生卒年月、简历、亲戚关系），俺也参考了天朝政府的官方网站，以及墙内的“百度百科”。


== 下载说明 ==

GitHub 提供了“下载整个项目”的功能，但是会比较大。

如果你仅仅想看《太子党关系网络》这份文档，只需在首页上方点击进入 '''download''' 这个目录。

该目录下有 '''pdf''' 和 '''jpg''' 两个子目录，分别存放对应的 '''【文件类型】''' 。你想要看哪一种文件格式，就进入哪个子目录里面。

进入【文件类型】的子目录之后，会看到一个文件列表（目前有13个文件）。先点击你想要的某个文件，会进入该文件的页面。

然后在【右上方】你会看到一个 '''Raw 按钮''' ，在这个按钮上点【右键】，在【右键菜单】里面选“保存”或“另存为”，就可以把这个文件下载到你本机。


== 多人协作说明 ==

俺非常希望有更多的网友参与该项目，大伙儿一起来完善天朝权贵家族的资料。

想要参与的同学，可以通过如下方式：

* 到[https://program-think.blogspot.com/ 俺博客]留言进行反馈，补充信息或反馈错误。

* 在[https://github.com/programthink/zhao/issues 本项目发一个 issue]，补充信息或反馈错误。

* Fork 该项目，进行修改，然后向俺发一个 Pull Request

（后面两种方式，你需要有 GitHub 的帐号）


== 数据格式说明 ==

本项目的数据文件，全部采用[https://zh.wikipedia.org/wiki/YAML YAML 格式]。这种格式非常简洁明了，有利于完全不懂技术的网友参与编辑。

而且俺在每一个 YAML 格式的文件中都写了详细的注释，便于其他网友修改。


== 目录说明 ==

=== data 目录 ===

data 目录用来保存数据文件，该目录下另有如下三个子目录：

* person

这个目录存放个人的资料，每个人一个目录，目录名就是人名。对于偶尔有同名的情况，在目录名末尾追加数字序号来区分。

每个目录下都有一个 brief.yaml 文件，包含此人的简介。

有些目录下还有一个 portrait.png 文件，对应此人的头像。

* company

这个目录存放与太子党有关的公司或组织机构。目录结构与 person 类似。

* family

这个目录存放家族关系的信息。每个家族是一个 yaml 格式的文件。

=== bin 目录 ===

该目录存放编译脚本。该脚本的使用参见下面的章节。

=== download 目录 ===

该目录存放制作好的文件，目前先提供 jpg 和 pdf 两种格式。

如果你需要其它格式，可以用 bin 目录下的编译脚本自行搞定（编译脚本的使用，参见下面的章节）。


== 编译脚本使用说明 ==

（俺是在 Linux 上编写该脚本，尚未在 Windows 上进行测试）

如果你在 Windows 上使用碰到问题，可以到[https://program-think.blogspot.com/ 俺博客]留言进行反馈。也可以在[https://github.com/programthink/zhao/issues 本项目发一个 issue]。

=== 脚本的命令行参数 ===

俺使用 python 作为编译脚本，该脚本位于 bin 目录下。

通过该脚本可以把原始数据生成为 dot 语言的脚本。然后再调用 Graphviz 把 dot 脚本生成各种格式（比如：pdf、jpeg）。

要使用该脚本，先在命令行模式下进入 bin 目录，然后运行如下命令：

（生成 pdf 格式的示例）

'''python make.py pdf'''

（生成 jpg 格式的示例）

'''python make.py jpg'''

=== 依赖的软件 ===

要使用上述脚本，你需要事先安装相关的软件（如下）

* Python（2 或 3）

因为俺用的是 Python 脚本，所以你需要先安装 python 软件。

目前 Python 有两种大版本——python2 和 python3——俺的编译脚本 '''【同时兼容】''' 这两种 Python 的大版本。

对于 Python 的小版本，俺本人在 '''2.7''' 和 '''3.5''' 上测试通过。2.6 和 3.4 估计也可以。

* PyYAML

这是一个基于 python 开发的软件包，专门用来处理 YAML 格式的文件。

你需要在你的 python 环境中安装该软件包。其官方链接如下：

[http://pyyaml.org/wiki/PyYAML PyYAML 的官网的 wiki]

[https://pypi.python.org/pypi/PyYAML Python 官网的 PYPI]

* Graphviz

这个软件是用来生成【关系图】的。关于该这个软件，俺已经写了一篇扫盲教程：

《[https://program-think.blogspot.com/2016/02/opensource-review-graphviz.html 开源项目：【自动】绘图工具Graphviz——《太子党关系网络》就是用它制作]》


== 致“反对此项目的墙内程序员” ==

本项目上线第二天，就收获 363 个 star 兼 88 个 fork，甚至还挤进 GitHub 的“当日 Trending”——俺很荣幸，也很高兴有这么多人给俺捧场。

但是在[https://github.com/programthink/zhao/issues 本项目的 issue 列表]中也看到好几个反对此项目的程序员（应该都来自墙内），他们担心这个项目导致 GitHub 被 GFW 封杀。

这几年来，类似的言论俺已经看了不少。就好比强盗拿刀杀人，围观者不但没有谴责强盗，反而去谴责卖刀的店家——这就是传说中的“斯德哥尔摩综合症”。

有兴趣的同学，可以看俺之前的博文——《[https://program-think.blogspot.com/2012/06/stockholm-syndrome.html 天朝民众的心理分析：斯德哥尔摩综合症]》
