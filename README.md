## 1.1 Spike-driven Transformer的特点
- 事件驱动：当Transformer的输入为零时，不触发计算。
- 二进制脉冲通信：所有与脉冲矩阵相关的矩阵乘法可以转化为稀疏加法。
- 自注意力具有线性复杂度：在token和通道维度上都具有线性复杂度。
- 操作：spike-form的Query、Key和Value之间的操作是掩码和加法。

## 1.2 主要内容
- 提出了一种新型的Spike-driven Transformer，它只利用稀疏加法，首次将spike-driven范式整合到Transformer中，并且对神经形态芯片友好。
- 

<!--stackedit_data:
eyJoaXN0b3J5IjpbNDM2MzU4NTg3LDIwNzA2MDMyNl19
-->