# Large Language Models(LLMs) for Code

A collection of LLMs of Code.

**Continuous update.:running:**

If there are any **errors** or some **missing models**, please contact us [new issue](https://github.com/wanghanbinpanda/Large-Language-Models-for-Code/issues) or by e-mail:wanghanbin95@163.com.

## Contents

- [Code LLMs](#Code LLMS)

- [Timeline of Code LLMs](#Timeline of Code LLMs)

- [Parameters of Code LLMs](#Parameters of Code LLMs)

- [Models](#Models)

- [Improve Code LLMs](#Improve Code LLMs)

- [Dataset](#Dataset)

- [Benchmark](#Benchmark)

- [Future](#Future)

  

## Code LLMs

Large Language Models(LLMs) for Code.

The Code LLMs referred to here is a large language model specially trained for code-related tasks. Its training corpus may not only contain code, but also natural language. 

The Code LLMs here does not include the general large language model, although the general large language model also has the ability to complete code-related tasks.



## Timeline of Code LLMs





## Parameters of Code LLMs







## Models

- Codex [OpenAI] [2021.07] [Close]

  :page_with_curl:[Evaluating Large Language Models Trained on Code](https://arxiv.org/abs/2107.03374)

  :black_flag:[introduction](./Model/1-CodeX.md)

  ```yaml
  Model Architecture: Decoder Only,GPT Family
  Params: 12B
  Training Data: Collected[159GB]
  Training Time: -
  Languages: Python[Multilingual]
  Evaluation: HumanEval, APPS
  Supported Tasks: Code Generation，Docstring Generation
  ```


- Tabnine [Close]

  :black_flag:[introduction](./Model/2-Tabnine.md)

  ```yaml
  Model Architecture: LLM
  Params: -
  Training Data: -
  Training Time: -
  Languages: -
  Evaluation: -
  Supported Tasks: Whole line completions,Full-function completions,Natural language to code completions
  ```

- AlphaCode [DeepMind] [2022.03] [Close]

  :page_with_curl:[Competition-Level Code Generation with AlphaCode](https://arxiv.org/abs/2203.07814)

  :black_flag:[introduction](./Model/3-AlphaCode(DeepMind).md)
  
  ```yaml
  Model Architecture: Encoder-Decoder
  Params: 41B
  Training Data: Collected[Code: 715.1GB]
  Training Time: -
  Languages: 12langs
  Evaluation: HumanEval,APPS,CodeContest
  Supported Tasks: Competition-Level Code Generation
  ```

- PaLM-Coder [Google] [2022.04] [Close]

  :page_with_curl:[PaLM: Scaling Language Modeling with Pathways](https://arxiv.org/abs/2203.07814)

  :black_flag:[introduction](./Model/4-PaLM-Coder(Google).md)

  ```yaml
  Model Architecture: Decoder Only
  Params: 8B, 62B, 540B
  Training Data: Collected[Text: 741B tokens Code: 39GB(780B tokens trained)]
  Training Time: 6144 TPU
  Languages: Multiple
  Evaluation: HumanEval,MBPP,TransCoder,DeepFix
  Supported Tasks: Code Generation,Code Translation,Code Repa 
  ```

- PolyCoder [CMU] [2022.02] [[Open]](https://github.com/VHellendoorn/Code-LMs)

  :page_with_curl:[A Systematic Evaluation of Large Language Models of Code](https://arxiv.org/abs/2203.07814)

  :black_flag:[introduction](./Model/5-PolyCoder(CMU).md)

  ```yaml
  Model Architecture: Decoder Only，GPT Family
  Params: 2.7B
  Training Data: Collected[Code: 253.6GB]
  Training Time: - 
  Languages: 12 langs
  Evaluation: HumanEval
  Supported Tasks: Code Generation
  ```


- GPT-Neo [EleutherAI] [2021.03] [[Open]](https://github.com/EleutherAI/gpt-neo)

  :page_with_curl:GPT-Neo: Large Scale Autoregressive Language Modeling with Mesh-Tensorflow

  :black_flag:[introduction](./Model/6-GPT-Neo.md)

  ```yaml
  Model Architecture: Decoder Only,GPT Family
  Params: 1.3B, 2.7B
  Training Data: The Pile[Text: 730GB Code: 96GB(400B tokens trained)]
  Training Time: -
  Languages: Multiple
  Evaluation: HumanEval
  Supported Tasks: Code Generation
  ```


- GPT-NeoX [EleutherAI] [2022.04] [[Open]](https://github.com/EleutherAI/gpt-neox)

  :page_with_curl:[GPT-NeoX-20B: An Open-Source Autoregressive Language Model](https://arxiv.org/abs/2204.06745)

  :black_flag:[introduction](./Model/7-GPT-NeoX.md)

  ```yaml
  Model Architecture: Decoder Only,GPT Family
  Params: 20B
  Training Data: The Pile[Text: 730GB Code: 95GB(473B tokens trained)]
  Training Time: -
  Languages: Multiple
  Evaluation: HumanEval
  Supported Tasks: Code Generation
  ```

- GPT-J [EleutherAI] [2021.06] [[Open]](https://github.com/kingoflolz/mesh-transformer-jax)

  :link:[GPT-J-6B: 6B JAX-Based Transformer](https://arankomatsuzaki.wordpress.com/2021/06/04/gpt-j/)

  :black_flag:[introduction](./Model/8-GPT-J.md)

  ```yaml
  Model Architecture: Decoder Only,GPT Family
  Params: 6B
  Training Data: The Pile[Text: 730GB Code: 96GB(473B tokens trained)]
  Training Time: -
  Languages: Multiple
  Evaluation: HumanEval
  Supported Tasks: Code Generation
  ```

- Incoder [Meta] [2022.04] [[Open]](https://sites.google.com/view/incoder-code-models/)

  :page_with_curl:[InCoder: A Generative Model for Code Infilling and Synthesis](https://arxiv.org/abs/2204.05999)

  :black_flag:[introduction](./Model/9-Incoder(Meta).md)

  ```yaml
  Model Architecture: Decoder Only
  Params: 1.3B,6.7B
  Training Data: Collected[Code: 159GB StackOverflow: 57GB(60B tokens trained)]
  Training Time: -
  Languages: 28 langs
  Evaluation: HumanEval,MBPP,CodeXGLUE
  Supported Tasks: Infilling Lines Of Code (HumanEval),Docstring Generation (CodeXGLUE), Return Type Prediction,Varible Name Predic
  ```

- CodeGen [Salesforce] [2022.03] [[Open]](https://github.com/salesforce/CodeGen) :star2:popular 

  :page_with_curl:[CodeGen: An Open Large Language Model for Code with Multi-Turn Program Synthesis](https://arxiv.org/abs/2203.13474)

  :black_flag:[introduction](./Model/10.11-CodeGen.md)

  ```yaml
  Model Architecture: Decoder Only
  Params: 6.1B, 16.1B
  Training Data: The Pile,BigQuery,BigPython[Code:150B tokens Text:355B tokens]
  Training Time: -
  Languages: CodeGen-Multi(6 langs),CodeGen-Mono(python)
  Evaluation: HumanEval, MTPB
  Supported Tasks: Single-Turn Code Generation,Multi-Turn Code Generation
  ```

- CodeGeeX [THU] [2022.09] [[Open]](https://github.com/THUDM/CodeGeeX)

  :page_with_curl:[CodeGeeX: A Pre-Trained Model for Code Generation with Multilingual Evaluations on HumanEval-X](https://arxiv.org/abs/2303.17568)

  :black_flag:[introduction](./Model/12-CodeGeeX(THU).md)

  ```yaml
  Model Architecture: Decoder Only,GPT Family
  Params: 13B
  Training Data: The Pile,CodeParrot,Collected[Code: 158B tokens(850B tokens trained)]
  Training Time: 1536 Ascend 910 AI processors (32GB) with Mindspore (v1.7.0),two months
  Languages: 23 langs
  Evaluation: HumanEval-X,HumanEval,MBPP,CodeXGLUE,XLCoST
  Supported Tasks: Multilingual Code Generation,Code Translation
  ```

- AiXcoder [PKU] [Close]

  :link:[AixCoder](https://www.aixcoder.com/#/)

  :black_flag:[introduction](./Model/14-AixCoder.md)

  ```yaml
  Model Architecture: -
  Params: 13B?
  Training Data: -
  Training Time: -
  Languages: Multiple
  Evaluation: -
  Supported Tasks: Code Generation,Code Completion,Code Search
  ```

- Pangu-Coder [Huawei Noah’s Ark Lab] [2022.07] [Close]

  :page_with_curl:[PanGu-Coder: Program Synthesis with Function-Level Language Modeling](https://arxiv.org/abs/2207.11280)

  :black_flag:[introduction](./Model/15-Pangu-Coder.md)

  ```yaml
  Model Architecture: PANGU-α architecture,Decoder Only
  Params: 2.6 B
  Training Data: Collected(147GB)
  Training Time: - 
  Languages: python
  Evaluation: HumanEval,MBPP
  Supported Tasks: Code Generation
  ```

- ERNIE-Code [Baidu] [2022.12] [Close]

  :warning:Don't think ERNIE-Code is a Code LLMs

  :page_with_curl:[ERNIE-Code: Beyond English-Centric Cross-lingual Pretraining for Programming Languages](https://arxiv.org/abs/2212.06742)

  :black_flag:[introduction](./Model/16-ERNIE-code.md)

  ```yaml
  Model Architecture: Encoder-Decoder,T5-base
  Params: 560M
  Training Data: CodeSearchNet,NL Corpus
  Training Time: - 
  Languages: Multiple
  Evaluation: mCoNaLa,Bugs2Fix,Microsoft Docs
  Supported Tasks: Multilingual Code-to-Text, Text-to-Code, Code-to-Code, and Text-to-Text Generation.
  ```

  


## Improve Code LLMs

- AlphaCode:[Competition-Level Code Generation with AlphaCode](https://arxiv.org/abs/2203.07814)
- CodeT:[CodeT: Code Generation with Generated Tests](https://arxiv.org/abs/2207.10397)



## Dataset

- **The Pile**

  :link:[repo](https://github.com/EleutherAI/the-pile):black_flag:[introduction](./Dataset/The-Pile.md)

- **BigQuery(BIGQUERY）**

  :link:[repo](https://cloud.google.com/bigquery/public-data?hl=zh-cn):black_flag:[introduction](./Dataset/BigQuery.md)

- **CodeParrot**

  :link:[repo](https://huggingface.co/datasets/codeparrot/github-code):black_flag:[introduction](./Dataset/CodeParrot.md)

- **The Stack**

  :link:[repo](https://huggingface.co/datasets/bigcode/the-stack):black_flag:[introduction](./Dataset/The-Stack.md)

- **PolyCoder**

  :link:[repo](https://github.com/VHellendoorn/Code-LMs):black_flag:[introduction](./Dataset/PolyCoder.md)

- **CodeSearchNet**

  :link:[repo](https://github.com/github/CodeSearchNet):black_flag:[introduction](./Dataset/CodeSearchNet.md)

- **ProjectCodeNet**

  :link:[repo](https://github.com/IBM/Project_CodeNet):black_flag:[introduction](./Dataset/ProjectCodeNet.md)

- **BigPython**

  :closed_lock_with_key:close:black_flag:[introduction](./Dataset/BigPython.md)

- **Collected**

  :spider:crawled data:black_flag:[introduction](./Dataset/Collected.md)




## Benchmark

- **HumanEval** 

  :link: [repo](https://github.com/openai/human-eval):page_with_curl:[paper](https://arxiv.org/abs/2107.03374):black_flag:[introduction](./Benchmark/HumanEval.md)

- **APPS**

  :link: [repo](https://github.com/hendrycks/apps):page_with_curl:[paper](https://arxiv.org/pdf/2105.09938.pdf):black_flag:[introduction](./Benchmark/APPS.md)

- **MBPP**

  :link: [repo](https://github.com/google-research/google-research/tree/master/mbpp):page_with_curl:[paper](https://arxiv.org/abs/2108.07732):black_flag:[introduction](./Benchmark/MBPP.md)

- **CodeXGLUE**

  :link: [repo](https://github.com/microsoft/CodeXGLUE):page_with_curl:[paper](https://arxiv.org/abs/2102.04664):black_flag:[introduction](./Benchmark/CodeXGLUE.md)

- **CodeContest**

  :link: [repo](https://github.com/deepmind/code_contests):page_with_curl:[paper](https://arxiv.org/abs/2203.07814):black_flag:[introduction](./Benchmark/CodeContest.md)

- **TransCoder**

  :link: [repo](https://github.com/facebookresearch/TransCoder):page_with_curl:[paper](https://arxiv.org/pdf/2006.03511.pdf):black_flag:[introduction](./Benchmark/TransCoder.md)

- **DeepFix**

  :link: [repo](https://bitbucket.org/iiscseal/deepfix/src/master/):page_with_curl:[paper](https://ojs.aaai.org/index.php/AAAI/article/view/10742):black_flag:[introduction](./Benchmark/DeepFix.md)

- **MTPB**

  :link: [repo](https://github.com/salesforce/CodeGen/tree/main/benchmark):page_with_curl:[paper](https://arxiv.org/abs/2203.13474):black_flag:[introduction](./Benchmark/MTPB.md)

- **HumanEval-X**

  :link: [repo](https://github.com/THUDM/CodeGeeX/blob/main/codegeex/benchmark/README_zh.md):page_with_curl:[paper](https://arxiv.org/abs/2303.17568):black_flag:[introduction](./Benchmark/HumanEval-X.md)

- **XLCoST**

  :link: [repo](https://github.com/reddy-lab-code-research/XLCoST):page_with_curl:[paper](https://arxiv.org/pdf/2206.08474.pdf):black_flag:[introduction](./Benchmark/Xlcost.md)

- **DS-1000**

  :link: [repo](https://ds1000-code-gen.github.io/):page_with_curl:[paper](https://arxiv.org/abs/2211.11501):black_flag:[introduction](./Benchmark/DS-1000.md)

- **ODEX**

  :link: [repo](https://github.com/zorazrw/odex):page_with_curl:[paper](https://arxiv.org/pdf/2212.10481.pdf):black_flag:[introduction](./Benchmark/ODEX.md)





## Future

- 
