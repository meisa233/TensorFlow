关于one hot的讲解<br />
>
https://blog.csdn.net/wenqiwenqi123/article/details/78055740
>
具体如下<br />
```
tensorflow中tf.one_hot()函数的作用是将一个值化为一个概率分布的向量，一般用于分类问题。

具体用法以及作用见以下代码：

import numpy as np
import tensorflow as tf
 
SIZE=6
CLASS=8
label1=tf.constant([0,1,2,3,4,5,6,7])
sess1=tf.Session()
print('label1:',sess1.run(label1))
b = tf.one_hot(label1,CLASS,1,0)
with tf.Session() as sess:
    sess.run(tf.global_variables_initializer())
    sess.run(b)
    print('after one_hot',sess.run(b))
最后的输出为：
label1: [0 1 2 3 4 5 6 7]
after one_hot:

 [[1 0 0 0 0 0 0 0]
 [0 1 0 0 0 0 0 0]
 [0 0 1 0 0 0 0 0]
 [0 0 0 1 0 0 0 0]
 [0 0 0 0 1 0 0 0]
 [0 0 0 0 0 1 0 0]
 [0 0 0 0 0 0 1 0]
 [0 0 0 0 0 0 0 1]]

--------------------- 
作者：超屌的温jay 
来源：CSDN 
原文：https://blog.csdn.net/wenqiwenqi123/article/details/78055740 
版权声明：本文为博主原创文章，转载请附上博文链接！
```
