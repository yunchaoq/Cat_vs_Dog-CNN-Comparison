# Cat_vs_Dog-CNN-compare
我选择的是16年Kaggle的猫狗大战数据集。之所以选择这个数据集，是因为自己一直很想把不同的网络方法，AlexNet，VGG16，ResNet50等等放在一起，做一个比较（就那种各种方法结果放在一张图里的，特别酷炫）。</br>
所以这次涉及到的代码量就比较多，之后的论述中就只粘贴核心代码部分。如果是我直接使用别人现成的模型或者代码，我也会注上网址。毕竟相比很多大牛，我还算一个门都没入的小白。
## 实验内容
### 数据集简介
数据集来源于此[Kaggle官网](https://www.kaggle.com/c/dogs-vs-cats-redux-kernels-edition)</br>
训练集有25000张，猫狗各占一半。测试集12500张，没有标定是猫还是狗。</br>
有大佬对数据本身做了一个分布的调查，分布结果如下(https://www.jianshu.com/p/1bc2abe88388)</br>
训练集中图片的尺寸散点分布图：</br>
![image](https://github.com/Mr-strlen/Cat_vs_Dog-CNN-compare/blob/master/Images/scatter_diagram_train_dataset.png)</br>
测试集中图片的尺寸散点分布图：</br>
![image](https://github.com/Mr-strlen/Cat_vs_Dog-CNN-compare/blob/master/Images/scatter_diagram_test_dataset.png)</br>
可以发现图像的大小存在着差异性，这就需要我们上来对图像进行一定的预处理。</br>
还有大佬发现，存在部分过于难识别的图像，通过手动删除的方式进行预处理，这里我觉得很有意思，也贴在这，但是之后的实验并没有进行数据的剔除。</br>
![image](https://github.com/Mr-strlen/Cat_vs_Dog-CNN-compare/blob/master/Images/image_movement.png)
