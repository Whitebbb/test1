# 1 文献阅读与知识准备
[参考文献链接](https://github.com/BICLab/Spike-Driven-Transformer)
## 1.1 文献主要内容
- 提出了一种新型的Spike-driven Transformer，它只利用稀疏加法，首次将spike-driven范式整合到Transformer中，并且对神经形态芯片友好。
- 设计了一种Spike-Driven Self-Attention (SDSA)，它只使用掩码和加法操作，没有乘法，从而比传统的自注意力机制有高达87.2倍的计算能效降低。
-   重新设计了Transformer中的残差连接，确保所有神经元通过二进制脉冲信号进行通信。
-   在静态和神经形态数据集上进行了广泛的实验，证明了所提出架构的有效性和效率。
## 1.2 Spike-driven Transformer
### 1.2.1  Spike-driven Transformer的特性
- 事件驱动：当Transformer的输入为零时，不触发计算。
- 二进制脉冲通信：所有与脉冲矩阵相关的矩阵乘法可以转化为稀疏加法。
- 自注意力具有线性复杂度：在token和通道维度上都具有线性复杂度。
- 操作：spike-form的Query、Key和Value之间的操作是掩码和加法。

### 1.2.2 Overall Architecture
### 1.2.3 Spike-Driven Self-Attention (SDSA)




# 2 实验记录


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTczODM0MjkzNSwxMjE2NDY5MTA3LC0xNT
I0MTI3NzEsLTI0NzkxMzAzMSwtMTgwOTg0NzA0NCw3OTMwMzky
NTMsMjA3MDYwMzI2XX0=
-->