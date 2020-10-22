## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/tnge123/tnge.github.io/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

@[TOC](用python画N和NS正态分布曲线)
# 代码展示
python入门水平，正在学习中，如果有错误也请多多指教~
这篇文章写作的目的首先是为了记录自己学习的过程，其次也是以讲解代码教学的形式，让自己印象更深刻一点。
今天的代码两个星期前就做好了，一直没有找到合适的web展示和讲解，拖延狗就是我。
```
import math
import numpy as np
import matplotlib.pyplot as plt

u = 0   
w = 2   
sig = math.sqrt(1) 
x = np.linspace(u - 3*sig, u + 3*sig, 50)   
m = np.linspace(w - 5*sig, w + 5*sig, 50)  
y = np.exp(-(x - u) ** 2 / (2 * sig ** 2)) / (math.sqrt(2*math.pi)*sig) 
n = np.exp(-(m - w) ** 2 / (2 * sig ** 2)) / (math.sqrt(2*math.pi)*sig) 
plt.plot(x, y, "g", linewidth=2)    
plt.plot(m, n, "g", linewidth=2)    
plt.grid(True)  # 加入网格线
plt.legend(loc='upper left')   
plt.plot(x, y, color='#FF0000')   
plt.show()
```
# 代码讲解
首先要插入我们的三个模块*math*模块*numpy*还有*matplotlib*
math是数学运算模块，numpy功能多一些，matplotlib模块用来画图，简称plt，

```
import math
import numpy as np
import matplotlib.pyplot as plt

u = 0   # 均值μ 这里我们设定为0 
w = 2   #这里我们设定均值为2
sig = math.sqrt(1)  # 标准差δ设定为1
x = np.linspace(u - 3*sig, u + 3*sig, 50)   # 定义域（-3，+3）
m = np.linspace(w - 5*sig, w + 5*sig, 50)   # 同上
y = np.exp(-(x - u) ** 2 / (2 * sig ** 2)) / (math.sqrt(2*math.pi)*sig) # 定义曲线函数
n = np.exp(-(m - w) ** 2 / (2 * sig ** 2)) / (math.sqrt(2*math.pi)*sig) # 定义曲线函数
plt.plot(x, y, "g", linewidth=2)    # 加载曲线（绘制出来）
plt.plot(m, n, "g", linewidth=2)    # 加载曲线
plt.grid(True)  # 加入网格线
plt.legend(loc='upper left')   #横纵坐标
plt.plot(x, y, color='#FF0000')   #加入颜色
plt.show()
```
![file-setting
](https://img-blog.csdnimg.cn/20201019004403957.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3RuZ2UxMjM=,size_16,color_FFFFFF,t_70#pic_center)
注意：模块是要先下载的（file-setting点击加号就可以了），可以搜索自己学要的模块进行展示。
运行结果如下
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201019004723845.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3RuZ2UxMjM=,size_16,color_FFFFFF,t_70#pic_center)
红色为N，绿色为NS

# 个人感觉
python的编写并没有很难，上手比较简单，重要的是理解代码的意思，熟悉代码的逻辑，下次想用的时候能会用才是最重要的！晚安了~

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/tnge123/tnge.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
