# CodeT [Microsoft] [2022.07] [Open]

Paper:[CodeT: Code Generation with Generated Tests](https://arxiv.org/abs/2207.10397)

```yaml
Model Architecture: 
Params:
Training Data:
Training Time:
Languages:
Evaluation: HumanEval,MBPP,APPS,CodeContests
Supported Tasks:
```



## Summary

对于给定的编程问题生成代码解决方案的任务可以从使用预训练语言模型（如Codex）中受益，该模型针对同一问题可以生成多个不同的样本。但是，这项任务的一个**主要挑战是从预训练语言模型生成的多个样本中选择最合适的解决方案**。评估代码解决方案的质量和正确性的一种自然方法是运行一组测试用例，但是手动创建这样的测试用例通常是昂贵和耗时的。在本文中，我们提出了一种新的方法CODET，**它利用同样的预训练语言模型来自动生成用于代码样本的测试用例，从而减少人力成本并增加测试场景的覆盖范围。**CODET使用生成的测试用例执行代码样本，并执行双重执行协议，考虑输出在生成的测试用例中的一致性以及与其他代码样本的一致性。我们使用五个不同大小和能力的预训练语言模型对四个基准数据集HumanEval、MBPP、APPS和CodeContests进行了全面的实验。我们的结果显示，CODET可以显着提高代码解决方案选择的性能，相对于以前的方法，实现了显著和一致的收益，且在不同模型和基准数据集上均表现出色。例如，CODET在HumanEval上将pass@1指标提高到65.8％，相对于code-davinci-002模型有18.8％的绝对改进，相对于以前的最新成果的绝对改进超过20％。
