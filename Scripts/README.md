# 练习小脚本

记录在生活、学习及工作中利用R编写的小脚本！

[>>返回R学习笔记主页!](https://github.com/Happykelee/the-Study-of-R)

1. **[读取网页菜单](01_GetMenu.R)**
    * **2018/01/31 记录**

    某年某月某日，部门经理要求同事将某饭店的菜单整理成表格供她挑选。由于饭店的所有菜品都放在了某点评的网页上，手动一个一个弄极为麻烦。反正菜单页面为静态网页，当前所学足够用，所以就写个小脚本弄了一个xls形式的[菜单表](01_menu.xls)。


2. **[计算染色体非整倍体的嵌合比例](02_MosiacRatio.R)**
    * **2018/01/31 记录**

    虽然在BerryGenomics作临床数据分析和解读，根本就不需要怎么编程（被招我的HR坑了），显然这并不是我选择这份工作的初衷。所以，用自己三脚猫的水平抽空解决一个工作中的小问题——计算染色体的嵌合比例。

    **读入文件要求**：包含一个批次的所有染色体比例的xls表格；  
    **重大的问题**：如果一个批次中的样本数较少，且大多数样本都是非整倍体（如：一个批次就24个样本，3/1以上的样本都是45X），相关染色体比例将严重偏离正常值。原因是脚本中各染色体比例的参考值是通过chr.stats()函数剔除偏离值（通常就是非整倍体样本或者数据波动很大的样本）后取均值，如果批次中的大部分样本都是问题样本，用这个想剔也剔不了。*不过这种情况很少见，就懒得改了。*  
    **另**，具体的文件存放的服务器IP地址匿了。
