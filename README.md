MultiFill
====================

A sublime text plugin to multi-fill text.

With this plugin, you can press <code>[ctrl+m]</code> and <code>[ctrl+f]</code> (short for Multi-Fill), when you use the sublime choose multi-place, to select a text type to fill multi-place automatically. And you can customize the texts to fill easily by edit the config file.


Formula insert
--------------------

If you just want to insert some numbers with your law, you can try <code>[ctrl+m]</code> and <code>[ctrl+i]</code> (short for Multi-Interger), to input your formula like this :
<pre>y = 2000 - 10x</pre>
the x is form 0 to how many places you selected, and the every place will be filled with 2000 1990 1980 ... etc. just the result of the formula you typed.

It will be very useful, while we write .html .sql and so on.


Multi select
--------------------

Now you can free your <code>ctrl + D</code>
    
We will not be cautious any more while we use <code>[ctrl+d]</code> to make multiple
selections. we can use the <code>[ctrl+alt+d]</code> to save the points and
selections now, and use <code>[ctrl+alt+enter]</code> to restore all of it.


Multi switch
--------------------

First, you can switch to the prev or next editor view by <code>[alt+left]</code> and <code>[alt+right]</code>. 

While you are using Split Editing, you can jump to the the prev or next window by <code>[ctrl+alt+left]</code> and <code>[ctrl+alt+right]</code>.

last, you can also jump with your view by <code>[ctrl+alt+shift+left]</code> and <code>[ctrl+alt+shift+right]</code>. 


Using Screenshot
====================

Fill ordered numbers
--------------------

you can choose to fill the multi-place with numbers increase.

![image](https://github.com/Lellansin/MultiFill/raw/master/screenshots/multi_fill_num.png)

Auto fill names
--------------------

you can fill the multi-place with ordered names (you can config the names manually, or set it random appear, see the bottom of the article for more detail..).

![image](https://github.com/Lellansin/MultiFill/raw/master/screenshots/multi_fill_names.png)

Random fill
--------------------

it can random insert the text as you can see:

![image](https://github.com/Lellansin/MultiFill/raw/master/screenshots/multi_fill_sex.png)


Customize easily
====================

you can easily customize the MultiFill's text type title and content as you wish.

the config file is <code>MultiFill.sublime-settings</code> it seems like:
<pre>
{
	"custom":
	[
		// you can edit the default
		{
			"name"  : "Names (ordered)",
			"way"   : "ordered",
			"values": 
			[
				"Alan","Bob","Cici","David","Elisabeth","Franklin"
			]
		},
		{
			"name"  : "Gender (random)",
			"way"   : "random",
			"values": 
			[
				"male","female"
			]
		},
		{
			"name":"V Roman (ordered)",
			"way"   : "ordered",
			"values":
			[
				"I","II","III","IV","V","VI","VII","VIII","IX","X","XI","XII"
			]
		}  
		// you can add your new here
		,{
			"name":"My text (ordered)",
			"way"   : "ordered",
			"values":
			[
				"test1","test2","test3","test4","test5","test6"
			]
		}

	]
}
</pre>


Wait Help
--------------------

Um, I must tell you a truth that today is the second day I use python (that's really an amazing language XD), and the code I wrote seems bad, so if is okay could you help to improve this plugin, thanks a lot XD



MultiFill
====================

多处操作的专用插件。


配置填充
--------------------

主要作用就是在选中多出的时候能够自动填充设置好的文字和数字。

当你选中多处之后按下 <code>[ctrl+m]</code> 和 <code>[ctrl+f]</code>，就可以调出 MultiFill 的主界面，你可以通过这个界面选择要填充的类型


公式填充
--------------------

如果你只是想按照某种规律来填充数字的话，推荐你使用 <code>[ctrl+m]</code> 和 <code>[ctrl+i]</code> ，接在出现的输入框中输入的你的公式即可：
<pre>y = 2000 - 10x</pre>
这个条公式就会在你选中的多处中依次填充 2000 1990 1980 ... 等等


多处选择
--------------------

再也不用再小心翼翼的使用 <code>[ctrl+d]</code> 来选中多个了，你可以用 <code>[ctrl+alt+d]</code> 来保存你当前的坐标和选中项位置，然后慢慢悠悠的使用键盘的方向键找到你要继续选中的东西之后再使用 <code>[ctrl+alt+enter]</code> 来恢复你的所有选中。


多屏切换
--------------------

单个窗口组中可以使用 <code>[alt+left]</code> 和 <code>[alt+right]</code> 在多个编辑页中左右切换（于 ctrl+PageUp 等的区别是不会跑到其他窗口组中）

如果你使用 <code>[alt+shitf+2]</code> 之类的多屏操作，你可以使用 <code>[ctrl+alt+left]</code> 和 <code>[ctrl+alt+right]</code> 在多个窗口组之前左右切换。

最后，你可以使用 <code>[ctrl+alt+shift+left]</code> 和 <code>[ctrl+alt+shift+right]</code> 带着你当前的编辑页一起跳到左右的窗口组中。


安装
--------------------
直接通过 package control 搜索 MultiFill 安装，如果没有 package control 请搜索 “sublime 插件” 然后先安装 package control。


配置文件在 【Preferences】->【Package Settings】->【MultiFill】 中，请参照 Setting - Default 来编写字节的 User - Default， 当然也可以直接在 Setting - Default 中修改
<pre>
{
	"custom":
	[
		{
			"name"  : "Names (ordered)", // 插入项名称(MultiFill界面显示)
			"way"   : "ordered",		 // 顺序插入
			"values": 	// 插入内容
			[
				"Alan","Bob","Cici","David","Elisabeth","Franklin"
			]
		},
		{
			"name"  : "Gender (random)",
			"way"   : "random",
			"values": 
			[
				"male","female"
			]
		},
		{
			"name":"V Roman (ordered)",
			"way"   : "ordered",
			"values":
			[
				"I","II","III","IV","V","VI","VII","VIII","IX","X","XI","XII"
			]
		},
		// 新添加一个试试
		{
			"name":"Names chinese (中文名称)",
			"way"   : "ordered",	// 顺序插入
			"values":
			[
				"张三", "李四", "唐儒马"
			]
		}
	]
}
</pre>

配置之后，有图有真相：

![image](https://github.com/Lellansin/MultiFill/raw/master/screenshots/add_chinese.png)
