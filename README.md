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
Spike-driven Transformer的概览，它包括四个部分：
1. 脉冲驱动编码器（SPSpike Patch Splitting, SPS）
2. Spike-Driven Self-Attention (SDSA)
3. 多层感知器（Multi-Layer Perceptron, MLP）
4. 线性分类（Classification Head）
### 1.2.3 Spike-Driven Self-Attention (SDSA)
**SDSA**利用掩码（mask）和稀疏加法操作来替代传统的矩阵乘法，从而在计算过程中几乎不消耗能量。这种方法特别适合于脉冲神经网络，因为它们在通信时只使用二进制脉冲（0或1）。
1.  **SDSA-V1**：在这个版本中，查询（Query, Q）和键（Key, K）首先执行元素级别的掩码操作，即哈达玛积（Hadamard product）。然后，通过列求和和脉冲神经元层来获得二进制的注意力向量，最后将这个二进制的注意力向量应用于值（Value, V）以掩码一些通道（特征）。
    
2.  **SDSA-V2**：这个版本揭示了SDSA是一种特殊类型的线性注意力机制，其中脉冲神经元层作为核函数。这种设计使得SDSA在token和通道维度上都具有线性的时间复杂度。



# 2 实验记录
## 2.1 数据准备
数据集


<!--stackedit_data:
eyJoaXN0b3J5IjpbNjM1NjMyOTI0LDE1MjQ5Mjg5NTQsMjg0MT
U4OTU2LC03MzgzNDI5MzUsMTIxNjQ2OTEwNywtMTUyNDEyNzcx
LC0yNDc5MTMwMzEsLTE4MDk4NDcwNDQsNzkzMDM5MjUzLDIwNz
A2MDMyNl19
-->