torch》linspace的使用

![image-20220712170349404](C:\Users\zhao'ming'zhang\AppData\Roaming\Typora\typora-user-images\image-20220712170349404.png)

反向传播

![image-20220630174757700](C:\Users\zhao'ming'zhang\AppData\Roaming\Typora\typora-user-images\image-20220630174757700.png)

#### 交叉熵损失函数原理详解（交叉熵损失和Softmax函数是标配）

![[公式]](https://www.zhihu.com/equation?tex=f_j%28z%29%3D%5Cfrac%7Be%5E%7Bz_j%7D%7D%7B%5Csum_ke%5E%7Bz_k%7D%7D)被称作softmax 函数（对输出的结果进行处理，使其分类的预测值的和为1)

https://blog.csdn.net/b1055077005/article/details/100152102

https://blog.csdn.net/tsyccnh/article/details/79163834

#### 理解逻辑回归（逻辑回归不是回归，是分类）

逻辑回归是用回归的思想来解决二分类问题，逻辑回归的判别函数一般采用sigmod函数

sigmod函数：![image-20220705164558814](C:\Users\zhao'ming'zhang\AppData\Roaming\Typora\typora-user-images\image-20220705164558814.png)

因为g(z)函数的特性,它输出的结果也不再是预测结果,而是一个值预测为正例的概率,预测为负例的概率就是1-g(z).

,我们得到一个回归函数,它不再像y=wT * x一样受离群值影响,他的输出结果是样本预测为正例的概率(0到1之间的小数).我们接下来解决第二个问题:选定一个阈值.

https://blog.csdn.net/weixin_39445556/article/details/83930186

#### 神经元及其激活函数

https://zhuanlan.zhihu.com/p/21462488?refer=intelligentunit

rule这个激活函数之所以会让神经元死亡，是因为对于一个特别的输入，梯度下降后更新参数，参数更新的不合适，对于一个输入后输出都是0，相当于神经元死亡了，所以要检测好神经元的死亡情况，正确设置好学习率。

#### Dropout的理解

dropout主要是为了防止过拟合问题，通过设置一个概率p使得激活函数值为0，从而屏蔽掉一定的神经元。

https://blog.csdn.net/program_developer/article/details/80737724

损失：MSE、RMSE、MAE、MAPE、SMAPE

https://blog.csdn.net/guolindonggld/article/details/87856780

#### RNN(循环神经网络)

![image-20220712114431194](C:\Users\zhao'ming'zhang\AppData\Roaming\Typora\typora-user-images\image-20220712114431194.png)

![image-20220712114626480](C:\Users\zhao'ming'zhang\AppData\Roaming\Typora\typora-user-images\image-20220712114626480.png)

![image-20220712115439116](C:\Users\zhao'ming'zhang\AppData\Roaming\Typora\typora-user-images\image-20220712115439116.png)

![image-20220712115404221](C:\Users\zhao'ming'zhang\AppData\Roaming\Typora\typora-user-images\image-20220712115404221.png)

![image-20220712162558439](C:\Users\zhao'ming'zhang\AppData\Roaming\Typora\typora-user-images\image-20220712162558439.png)

#### 自然语言处理最基本的字符处理方式

![image-20220712163029821](C:\Users\zhao'ming'zhang\AppData\Roaming\Typora\typora-user-images\image-20220712163029821.png)

![image-20220712163132126](C:\Users\zhao'ming'zhang\AppData\Roaming\Typora\typora-user-images\image-20220712163132126.png)

h这里就是一个1×4的张量，输出o也是一个1×4的张量，然后利用交叉熵损失（交叉熵损失回自己进行softmax计算，得到各个维度上的值，然后进行分类）这里要区别好NLLoss损失，使用nllloss前边一般要有函数logsoftmax进行处理，其实就是和交叉熵损失一样了，只不过交叉熵损失把这几把集合了起来。

![image-20220712170449139](C:\Users\zhao'ming'zhang\AppData\Roaming\Typora\typora-user-images\image-20220712170449139.png)

![image-20220712170623718](C:\Users\zhao'ming'zhang\AppData\Roaming\Typora\typora-user-images\image-20220712170623718.png)
