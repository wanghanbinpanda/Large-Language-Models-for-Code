# ERNIE-Code [Baidu] [2022.12] [Close]

Paper:[ERNIE-Code: Beyond English-Centric Cross-lingual Pretraining for Programming Languages](https://arxiv.org/abs/2212.06742)

```yaml
Model Architecture: Encoder-Decoder,T5-base
Params: 560M
Training Data: CodeSearchNet,NL Corpus
Training Time: - 
Languages: Multiple
Evaluation: mCoNaLa,Bugs2Fix,Microsoft Docs
Supported Tasks: Multilingual Code-to-Text, Text-to-Code, Code-to-Code, and Text-to-Text Generation.
```



参数量太少，论文里都是与PLBART，CodeT5进行比较，没有与目前的主流模型进行比较。不过可以参考改论文中训练模型的方法，但使用的是T5-based 框架，可能后续不会follow.

而且测试用的benchmark，不是一些代码大模型常用的benchmark。

并不是一个很经典的Code LLMs，甚至不是一个Code LLMs。

