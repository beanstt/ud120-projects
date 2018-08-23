ud120-projects
==============

Starter project code for students taking Udacity ud120

## beanstt补充：

[来自](https://classroom.udacity.com/courses/ud120/lessons/2254358555/concepts/30199885720923)

检查你是否装有可用的 python，版本最好是 2.6 或 2.7（这是我们使用的版本 - 其他版本应该也可以，但我们不敢保证）。
我们会使用 pip 来安装一些包。首先，从[此处](https://pip.pypa.io/en/latest/installing.html)获取并安装 pip。
使用 pip 安装一系列 Python 包：

转到终端行界面（请勿打开 Python，只打开命令提示符）

安装 sklearn: pip install scikit-learn

[此处](http://scikit-learn.org/stable/install.html)包含 sklearn 安装说明，可供参考

安装自然语言工具包：pip install nltk

获取机器学习简介源代码。你将需要 git 来复制资源库：git clone https://github.com/udacity/ud120-projects.git
你只需操作一次，基础代码包含所有迷你项目的初始代码。进入 tools/ 目录，运行 startup.py。该程序首先检查 python 模块，然后下载并解压缩我们在后期将大量使用的大型数据集。下载和解压缩需要一些时间，但是你无需等到全部完成再开始第一部分。


## beanstt补充：（练习：作者身份准确率）

在 naive_bayes/nb_author_id.py 中创建和训练朴素贝叶斯分类器，用其为测试集进行预测。准确率是多少？

在训练期间，你可能会看到以下错误：“用户警告：分数重复。结果可能取决于特征排序，或者你对回归任务使用了分类分数。” 警告（“分数重复。结果可能取决于特征排序。”）

邮件中两个以上的单词恰巧具有相同的使用模式时，会出现这一警告—对算法而言，这表示两个特征是相同的。当重复特征出现时，一些算法实际上会中断（数学上无法运行），或给出多个不同的答案（取决于特征排序），然后 sklearn 发出警告。这种信息能起到帮助作用，所以我们无需担心。

[开始练习](https://classroom.udacity.com/courses/ud120/lessons/2254358555/concepts/30245185880923#)

在此问题中，一些学员在执行代码时会遇到内存问题。为了降低运行代码时看到内存错误的提示，我们建议你使用 RAM 至少为 2GB 的计算机。如果你发现代码造成内存错误，你也可以尝试在 email_preprocess.py 文件中设置 test_size = 0.5。


## beanstt补充：（练习：对NB分类器计时）

我们之前未明确提及的一个重要主题是何时训练和测试算法。在你分类器所在行的上方和下方插入两行代码，就像这样：
```
t0 = time()
< 你的 clf.fit() 代码行 >
print "training time:", round(time()-t0, 3), "s"
```

在你的 clf.predict() 代码行前后也加上这段代码，这样你可以比较训练分类器的所需时间，并作出预测。训练和预测哪一个更快？

我们会把朴素贝叶斯的用时与其他几种算法比较，所以请记下你得到的时间和准确率，在下一个迷你项目中，我们还会用到。

[开始练习](https://classroom.udacity.com/courses/ud120/lessons/2254358555/concepts/30127485730923#)


