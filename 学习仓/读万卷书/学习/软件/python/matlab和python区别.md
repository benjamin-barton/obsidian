Matlab
 
> z=0:100;  
> average(z)  
> function y = average(x)  
> if ~isvector(x)  
> error('input must be a vector')  
> end  
> y=sum(x)/length(x);  
> end
 
Python
 
> import datetime  
> def print_datetime():  
> print('task completed')  
>print(datetime.datetime.now())  
> print()
>  
> for x in range(0,10):  
> print(x)  
> print_datetime()
   

matlab把函数放在后面，python很正常，放前面就行  
Matlab 一个函数，输出是y 名字叫average，不需要冒号，但要有end  
Python 定义一个名字叫print-datetime的函数，有冒号，输出放在return里了

> def piece_wise_function(x):  
> if 90<=x<=100:  
> print(1)  
> elif 80<=x<=90:  
> print(2)  
> elif 60<=x<=80:  
> print(3)  
> elif 0<=x<=60:  
> print(4)  
> else:  
> print(0)  
> return 'ok'  
> print(piece_wise_function(float(input('number'))))



> function y=piece_wise_fun(x)  
> if x>=90 && x<=100  
> y=1;  
> elseif x>=80 && x<=90  
> y=2;  
> elseif x>=60 && x<=80  
> y=3;  
> elseif x>=0 && x<=60  
> y=4;  
> else  
> y=0;  
> end  
> end

matlab是elseif，函数不缩进，条件也没有冒号，但是不能连着整，完事呢要有end  
python是elif，得有冒号，不需要end，函数也不需要end，return也是可有可无

> name=['张芳睿','张曦元','蔡湘媛']  
> for idex in name:  
> print(idex)
>  
> for idex in range(0,5):  
> print(idex)  
> 输出还是没有5

python依旧要有冒号，列表里的一个个遍历  
matlab还是没有冒号，他把  
你在这里头挑  
转化成  
i等于这个到那个  
python想弄数就range创造一个数组  
啊你在数组里头挑，但matlab好像是子功能，他只能是数字，循环几次那种，  
这么看python>matlab

> for i=1:4  
> i  
> end  


人家matlab实诚，你说哪到哪就是哪到哪
 
> sum=0;  
> for i=1:5  
> sum_in=1;  
> for j=1:i  
> sum_in=sum_in*j;   
> end  
> sum=sum+sum_in;  
> end  
> Sum  
> 阶乘


在python里头索引步长被放在了后面，range也是一样

![Exported image](Exported%20image%2020250404144805-0.png)  
![Exported image](Exported%20image%2020250404144809-1.png)

在matlab里头  
没有什么从0开始，人老正常了，而且创建数组

![Exported image](Exported%20image%2020250404144810-2.png)

步长在中间，我更喜欢matlab多好理解  
为啥我没说matlab的索引呢，  
python索引是【】而matlab里是（）  
咱老是在里头搞矩阵  
矩阵他就有好几维，完了他就事儿多，比如  
[MATLAB](https://blog.csdn.net/weixin_46098577/article/details/110880673)学习笔记（一）数组的创建、索引及运算_matlab数组-CSDN博客

![Exported image](Exported%20image%2020250404144811-3.png)

a([1 3],[1 2])挺普遍的，行，列的交点  
a([2 3;1 2])感觉纯纯脑筋急转弯，合乎情理，他没有逗号  
本来我就数不明白单索引，我用它干啥

索引  
matlab，必须得是正数，你要从后面取不能用-1（在python里，-1是最后一项的意思）  
要用end，这个py里也能，但可以省略letters[19::4]就是从19到结尾，而且还能都省略  
letters[::7]，如果倒叙，那就是letters【-1：：-1】聪明的小玩意居然可以都省略letters【：：-1】，mat里呢？人家规规矩矩地array（end：-1：1）  
我更喜欢mat，而且矩阵整行都要的时候直接mat（：，1）  
py呢？也是这样，letters【：】如果带步长，才会两个冒号，  
这么简单得益于步长被放在了后面  
而mat则规规矩矩地mat（1：step：end）