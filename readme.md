# 基于卷积神经网络的手写数字识别
## install requirements
1. 从官网下载并安装anaconda3
2. 从anaconda navigator创建一个新的基于python3.7的环境

![](../statement/anaconda3.png)

3. open in terminal

![](../statement/terminal.png)

4. 在打开的的命令行工具中安装cuda和cudn以及pytorch

![](../statement/windows.png)

* 更换清华大学镜像

```
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
conda config --set show_channel_urls yes
```
* 配置完成后需要重新打开命令行

* 前往[pytorch官网](https://pytorch.org/get-started/locally/ "标题")选择对应的环境

![](../statement/pytorch.png)

* 比如我的是
```
conda install pytorch torchvision cudatoolkit=9.2 -c pytorch -c defaults -c numba/label/dev
```
### 自此安装完毕，另外还有缺少的一些包请自行使用pip进行安装
```
pip intall [the lack packages]
```
## 项目文件说明
1. 文件夹data中存放着google的MINST数据集，本人把其缓存到了本地
2. images 是本人用windows画图工具画的三个手写数字2、3、5
3. cnn.pkl ，本人将训练完毕后的模型参数保存在其中，用pytorch框架可直接载入使用
4. CNN手写数字识别.ipynb文件是代码文件，代码分为两部分，第一部分是训练模型，包括搭建卷积神经网络，一些基本函数以及载入数据集并训练模型。\
第二部分是用训练完成的模型测试自己手写的数字，因为自己手写的数字是rgb图像，\
所以其中还包括了把rgb图像转换为float类型的灰度图像

## 运行结果截图
1. 训练过程的部分结果

![](../statement/out1.png)

2. 测试自己画的数字

![](../statement/mytest.png)
