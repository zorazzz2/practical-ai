## A Transformer Framework Based Translation Task
- 一个基于Transformer网络结构的文本翻译模型
- 论文[Attention Is All You Need](https://arxiv.org/abs/1706.03762) 基于PyTorch的实现

## 1. 环境准备

```shell 
conda create -n transformer_translate python=3.10
conda activate transformer_translate

cd translate/
pip install torch -i https://pypi.tuna.tsinghua.edu.cn/simple/ 
pip install torchtext -i https://pypi.tuna.tsinghua.edu.cn/simple/ 
pip install de_core_news_sm-3.0.0.tar.gz -i https://pypi.tuna.tsinghua.edu.cn/simple/ 
pip install en_core_web_sm-3.0.0.tar.gz -i https://pypi.tuna.tsinghua.edu.cn/simple/ 
```

## 2. 使用方法

### 2.1 修改配置文件(可选)
可自定义修改配置文件`config.py`中的配置参数，也可以保持默认

### 2.1 训练
直接执行如下命令即可进行模型训练：
```
python train.py
```

训练过程：
```text
Epoch: 2, Train loss: 5.685, Train acc: 0.240947
Epoch: 2, Train loss: 5.668, Train acc: 0.241493
Epoch: 2, Train loss: 5.714, Train acc: 0.224682
Epoch: 2, Train loss: 5.660, Train acc: 0.235888
Epoch: 2, Train loss: 5.584, Train acc: 0.242052
Epoch: 2, Train loss: 5.611, Train acc: 0.243428
```
学习率变化：
<img src = "imgs/learning_rate.jpg" width="500" >


## 2.2 预测（inference）
直接运行如下命令即可：

```
python translate.py
```

示例结果：

```text
德语：Eine Gruppe von Menschen steht vor einem Iglu.
翻译：A group of people standing in fraon of an igloo .
英语：A group of people are facing an igloo.
=========
德语：Ein Mann in einem blauen Hemd steht auf einer Leiter und putzt ein Fenster.
翻译：A man in a blue shirt is standing on a ladder cleaning a window.
英语：A man in a blue shirt is standing on a ladder cleaning a window.
```

[//]: # (## 3. 结果)

[//]: # (bleu评测结果)

[//]: # ()
[//]: # (|val | test_2016_flickr |)

[//]: # (|--|--|)

[//]: # (| | |)
