# PaLM-Coder [Google] [2022.04] [Close]

Paper:[PaLM: Scaling Language Modeling with Pathways](https://arxiv.org/abs/2204.02311)

```yaml
Model Architecture: Decoder Only
Params: 8B, 62B, 540B
Training Data: Collected[Text: 741B tokens Code: 39GB(780B tokens trained)]
Training Time: 6144 TPU
Languages: Multiple
Evaluation: HumanEval,MBPP,TransCoder,DeepFix
Supported Tasks: Code Generation,Code Translation,Code Repa 
```

PaLM 540B 在单个模型中显示了横跨编码任务和自然语言任务的强大性能，即使它在预训练数据集中只有 5% 的代码。具体而言，PaLM 540B 的 few-shot 性能十分显著，与经过微调的 Codex 12B 相当，同时使用的 Python 训练代码减少到了 50 分之一。这一结果印证了之前的发现，即较大的模型比较小的模型更高效，因为它们可以更好地从其他编程语言和自然语言数据中实现迁移学习。

此外，通过在纯 Python 代码数据集上微调 PaLM ，模型进一步提高了性能，称之为 **PaLM-Coder**。



训练时对标准的 Transformer 架构做出了如下更改：

1. SwiGLU 激活
2. 并行层
3. 多查询（Multi-Query）注意力
4. RoPE 嵌入
5. 共享输入 - 输出嵌入
6. No Biases
7. 词汇表研究者创建了一个「无损（lossless）」词汇表，它保留了所有空格（对于代码来说尤其重要）
