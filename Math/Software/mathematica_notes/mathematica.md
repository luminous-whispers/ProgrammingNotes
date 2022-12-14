# <center> mathematica</center>
<center>软件说明:</center>
mathmetica支持直接将字母带入运算表达式中,回车代表换行,shift+enter是执行程序.mathmetica有强大的内建函数.  该软件区分大小写,请注意.
有分号会保留结果,没有分号才会输出结果.一行也可以写多个表达式,但是要以分号结尾.

### 1基础:   
 
* 1.1算数运算符:+-*/^![^2]

 [^2]:注意哦,xy不是乘积,x*y才是乘积.
 
* 1.2逻辑运算符:&&,||,!,==,!=
* 1.3特殊符号:%可以指代上一次的运算结果.
![基础程序形式图解](D:/yjw/vnote/计算机软件/图片/mathematica基础说明.png)
### 2常数与变量:
* 2.1 常数:
    1.虚数单位`I`
    2.圆周率`Pi`
    3.自然对数`E`
    4.无限大`Infinity`
* 2.2常数的转换:[^1]
    * N[x,n]将x转化为实数,n为精度位数,可以省略.
    * Rationalize[x,dx]将x转化为有理数,误差小于dx
    * NumberForm[x,n]将x以n位精度的实数输出.
    * ScientificForm[x]将x以科学计数法的形式输出 

[^1]:需要用到内建函数.

* 2.3变量:
    * 变量命名:不但能以数字开头,但是可以是字母和数字的组合.
    * 批量赋值:(数组赋值)&emsp;{x,y}={1,2}
    * 变量的替换：使用/.和->箭头可以用来替换表达式中变量的数值.执行f=2x只可以得到f=2x，再执行f/.x->2就可以得到4，也就是将式子中的x用2替换。多变量的时候用f/.{x->1,y->2}来用值替换变量。
    * 变量的删除：Clear[]可以用于删除一个变量，在Mathematic里面变量一旦定义就固定了，所以如果多次使用f这个字母可能出现问题，那么我们要定义新的f的时候就需要用Clear[f]将其删除后再重新定义，这点很重要，尤其是在程序变量很多的时候。

[^3]:再次强调一遍:mathematica区分大小写

### 3.函数:
* 3.1 常见内建函数:[^3]
    * ` Sin[],Cos[]`,`Log[]`
    * `Plot[]`用于函数绘制
    * `Expand[]`用于多项式展开
    * `Clear[]`用于删除一个变量,重新定义.
    * `Round[]`四舍五入
    * `Max[]`取最大值
    * `Exp[]`指数函数
* 3.2 自定义函数的用法:
    * f[x_]=表达式1
    * 多变量: f[x_,y_,z_]=
    * 延迟定义: f[x_]:= 现在写的只是一个式子，程序并不执行，等到你第一次调用该函数的时候系统才会真正定义
    * 分段函数定义:使用If[]实现
    &emsp;如:f[x_]=If[x>=0,x=x,x=x^2],这个else可以接着套if
 
[^4]:plot函数还需要更深入系统的学习.

* 3.3函数的调用与显示:
    * 函数调用:不需要替换,只需要直接在括号里赋值.如f[1]=...
    * 函数显示:Plot[f[x],{x,min,max}][^4]
    * 表:
### 4.方程
* 4.1数值解：
`Solve[{y==2x+3,y=3x-7},{x,y}]`
`NSolve[x^5-2x+3==0,x]`

















