# pygraphviz_install
问题：
1. pygraphviz在win10 64位下的pip和镜像安装都不支持；
2. graphviz官网提供的graphviz2.38不是64位的；

解决方案：

在github上下载64位版本的graphviz(https://github.com/mahkoCosmo/GraphViz_x64),因此版本缺少neato文件，所以还是要先在官网下载graphviz-2.38.msi文件安装。

1、安装graphviz-2.38.msi，安装位置是：C:\Program Files (x86)\Graphviz2.38\。

2、安装visual studio2017(教程见https://blog.csdn.net/aoe_xiu/article/details/87866675)。

3、把github下的x64文件中的lib目录下的所有文件复制到C:\Program Files (x86)\Graphviz2.38\lib\release\lib目录中，相同则替换；把github下的x64文件全部覆盖到C:\Program Files (x86)\Graphviz2.38。

4、安装pygraphviz(https://github.com/pygraphviz/pygraphviz)，其中替换三个文件：setup.py,graphviz_wrap.c和graphviz.i（在这里下载https://github.com/longwenxiu/pygraphviz_install）。

5、运行python setup.py install文件。

6、将C:\Program Files (x86)\Graphviz2.38\bin写入系统的path变量中。

7、进入python，输入import pygraphviz as pgv测试，未报错则成功安装。
--------------------- 
https://blog.csdn.net/aoe_xiu/article/details/87865867 



