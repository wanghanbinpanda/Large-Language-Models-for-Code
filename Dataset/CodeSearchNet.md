# CodeSearchNet

CodeSearchNet 语料库。这个语料库首先从 GitHub 收集了大量的公共和允许的存储库，然后用 Treesitter 进一步处理这些存储库，以提取函数 (方法) 和文档字符串对。该数据集包含了六种编程语言的配对:Go、Java、JavaScript、Python、PHP 和 Ruby。CodeBERT 和 CodeT5 使用该数据集进行预训练。