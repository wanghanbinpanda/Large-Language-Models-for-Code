# PolyCoder [CMU] [2022.02] [[Open]](https://github.com/VHellendoorn/Code-LMs)

Paper:[A Systematic Evaluation of Large Language Models of Code](https://arxiv.org/abs/2202.13169)

```yaml
Model Architecture: Decoder Only，GPT Family
Params: 2.7B
Training Data: Collected[Code: 253.6GB]
Training Time: - 
Languages: 12 langs
Evaluation: HumanEval
Supported Tasks: Code Generation
```

目前尽管代码大模型取得了非常不错的效果，但它们并不开源，这限制了一些资源匮乏的组织去研究这一领域。研究界也无法研究这些模型的其他关键方面，如可解释性、模型的蒸馏以获得更有效的部署，以及合并其他组件，如检索。

本论文发布了一个新的模型，PolyCoder，具有基于GPT-2架构的27亿参数，它在一台机器上跨12种编程语言的249GB代码上进行训练。首先，论文对PolyCoder、开源模型和Codex之间的训练和评估设置进行了广泛的比较。其次，在HumanEval基准上评估模型，并比较不同大小和训练步骤的模型效果如何，以及不同温度如何影响生成质量。最后，由于HumanEval只评估自然语言到Python的合成，我们在12种语言中的每一种中创建了一个未知的评估数据集，以评估不同模型的perplexity。据称，CodeX专注于Python代码合成，但CodeX在其他编程语言中的表现也令人惊讶，甚至比The Pile上训练的GPT-J和GPT-NeoX更好。尽管如此，在C编程语言中，PolyCoder模型比所有这些模型实现的困惑程度更低。

一般来说，更大的模型和更多的训练时间有利于性能。论文还认为，在某些语言中，GPT-Neo在某些语言中的表现表明，对自然语言文本和代码的训练可以有利于代码的建模。

