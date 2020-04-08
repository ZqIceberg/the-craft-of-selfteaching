### 学习体验
尤其需要仔细看看《Jupyterlab 的安装与配置》的《关于 Jupyter lab themes》这一小节 —— 否则，阅读体验会有很大差别

ESC：从编辑模式回到命令模式
A：在当前 Cell 之前插入一个 Cell
B：在当前 Cell 之后插入一个 Cell
DD：连续按两次 d 键，删除当前 Cell
Y：将当前 Cell 设置为 Code Cell
M：将当前 Cell 设置为 Markdown Cell
shift + 回车：运行当前 Cell 中的代码
shift + L：显示/隐藏代码行号
回车：当前 Cell 进入编辑模式

写这本书的时候，前后弄出来那么多 .ipynb 文件 —— 于是，到最后哪怕 “生成个目录” 这样看起来简单的活，若是会用正则表达式，就能几分钟完成；但若是不会，那就得逐一手工提取、排序、编辑…… 对我来说怎么可能不是刚需！

```python
import re
import os

files = [f for f in os.listdir('.') if os.path.isfile(f)]
files.sort()
for f in files:
    if '.ipynb' in f:
        with open(f, 'r', encoding = 'UTF-8') as file:
            str = file.read()
            pttn = r'"# (.*)"\n'
            r = re.findall(pttn, str)
            if len(r) > 0:
                print(f'> - [{f.replace(".ipynb", "")}（**{r[0]}**）]({f})') # 生成 markdown
```


### 不觉明历
学会一门编程语言之后，再学其它的就会容易很多 —— 而且，当你学会了其中一个之后，早晚你会顺手学其它的，为了更高效使用微软办公套件，你可能会花上一两天时间研究一下 VBA；为了给自己做个网页什么的，你会顺手学会 JavaScript；为了修改某个编辑器插件，你发现人家是用 Ruby 写的，大致读读官方文档，你就可以下手用 Ruby 语言了；为了搞搞数据可视化，你会发现不学会 R 语言有点不方便……

第一遍囫囵吞枣之后，马上就要开始 “总结、归纳、整理、组织 关键知识点” 的工作。自己动手完成这些工作，是所谓学霸的特点。他们只不过是掌握了这样一个其他人从未想过必须掌握的简单技巧。他们一定有个本子，里面是各种列表、示意图、表格 —— 这些都是最常用的知识（概念）整理组织归纳工具，这些工具的用法看起来简单的要死。

先关注使用再研究原理
作为人类，我们原本很擅长运用自己并不真正理解的物件、技能、原理、知识的……

预算观念非常重要 —— 这个观念的存在与否，成熟与否，基本上决定一个人未来的盈利能力。

Must have
Should have
Could have
Won't have


在学习编程的过程中，你会不由自主地学会一个重要技能：
#### 拆解
拆解的第一种方法是把某个任务拆分成若干个小任务，正如上面的讲解那样，我称它为 “横向拆解”
另外一种方法，我称它为 “纵向拆解”（有时，我也会用 “分层拆解” 这个说法）。
这种方式在自学复杂的概念体系时特别管用。

写这本书的时候，前后弄出来那么多 .ipynb 文件 —— 于是，到最后哪怕 “生成个目录” 这样看起来简单的活，若是会用正则表达式，就能几分钟完成；但若是不会，那就得逐一手工提取、排序、编辑…… 对我来说怎么可能不是刚需！

注意力漂移，是我杜撰的一个词，用来作为 “注意力集中” 的反义词 —— 因为更多的时候，我们并不是 “注意力不集中”，而是…… 而是更令人恼火的一个现象：
“注意力所集中的焦点总是不断被自己偷偷换掉……

=======兰圃计划培训========

/ 浮点除法
//整数除法

```
	who = 'my'
	name = 'harry'
sentence = f'{who} name is {name}'
```
但是一般常用的是str.format()
```
sentence = '{1} name is {0}'.format(who, name)
```

#### 创建实例
self
```python
class Week:
	mon = 'Mon'
	tue = 'Tue'

	def show_day(self, day):
			if day == 1:
				print(self.mon)
			else:
				print(self.tue)

week = Week()
week.show_day(1)
week.show_day(2)
week.tue = 'Tue Day2'
week.show_day(2)
```


#### 课上案例

binary_search，随时数生成，random.randint(1, 20),交互猜数
guess，通过GUI，画数轴的方式，表达猜数的过程。注意，写guidline_EN
guess_with_log，不清空画布，每次的画图过程保留
dictionary，python的字典
flip_coin，正反面硬币，ht = random.randint(0, 1)，来个随机数，取个模，模拟掷硬币的过程
dice.py，画坐标轴和折线，**这个不懂**
input.py，文字反馈输入的变量的类型
lq006.py，商品编号，**这个不懂**
split.py，切分数据
strip.py，去空格，去指定字符
Arithmetic_progression.py，举boss的例子，枚举a1-an,循环的写法，递归的写法
division.py，不带除号的除法，用减法实现。循环写法，递归写法
factorial.py，阶乘的循环写法，递归写法
max_value.py，循环写法，递归写法
nn.py，打印n个n，循环写法，两个参数写法，一个参数写法
times.py，n个数相加，循环写法，递归写法
ascii.py，ord('a')， chr(98)，ascii码
colon.py，打印格式，列表打印
exception.py，**这个不懂有啥场景**
file_organizer.py，创建文件，**这个不懂**
file_rename.py**这个不懂**
files.py，写入文件数据
join_os_join.py，文件路径的join
list_review.py，list,append数据进去
nums.py，用递归模拟数学计算过程，深刻理解数学
paint.py，一道真题，画一个钻石圆圈
slice.py，字符串操作，split
split.py，列表的正着取，倒着取，把字符串根据.进行分割
square.py，turtle画圆圈
string_stat.py，统计字符串中字符的个数
