# ODEX

ODEX是自然语言到代码生成的数据集。ODEX拥有945个自然语言和代码的对应组成的数据对，覆盖了79个不同的库，并包含了1,707个人工编写的执行测试用例。我们从StackOverflow论坛中获取了这些自然语言和代码的对应组成的数据对，以鼓励自然且实用的编码查询，并经过仔细的重新表述，以确保意图清晰并防止潜在的数据记忆。此外，ODEX支持四种自然语言作为意图，包括英语、西班牙语、日语和俄语。ODEX揭示了在执行自然语言到代码生成任务时，最优模型之间的行为差异：CODEX在开放域查询中表现更好，而CODEGEN在开放域和封闭域之间保持更好的平衡。ODEX验证了基于执行的评估相比不包含执行的评估指标的优点，同时揭示了它们的互补效应。像CODEGEN-6B这样的强大模型仅能在top-1预测中获得11.96的通过率，表明还有很大的提升空间。我们发布ODEX以促进代码生成社区对开放域问题的研究。





数据格式：

```json
{
    'task_id': 3844801,
    'intent': "check if all elements in list `myList` are identical", 
    'prompt': "def f_3844801(myList):\n\treturn ",
    'canonical_solution': "all(x == myList[0] for x in myList)",
    'suffix': "",
    'test_start': "\ndef check(candidate):",
    'test': [
        "\n    assert candidate([1,2,3]) == False\n", 
        "\n    assert candidate([1,1,1,1,1,1]) == True\n",
        "\n    assert candidate([1]) == True\n",
        "\n    assert candidate(['k','k','k','k','k']) == True\n",
        "\n    assert candidate([None,'%$#ga',3]) == False\n"
    ],
    'entry_point': "f_3844801",
}
```

task_id是原始StackOverflow帖子的帖子ID，样本从中构建而来；

intent是经过人工注释的自然语言描述，具有合格的特定性；

prompt是函数前缀（定义、输入参数等），以正确执行代码片段；

canonical_solution是编码问题的参考解决方案（由人工注释员验证）；s

uffix是函数后缀（返回值，如果有的话），以正确执行代码；

test_start是测试函数的定义，同时包括程序所需的库导入；

test是由人工注释员创建的测试用例列表；

entry_point是在评估期间应该调用的函数名称“check”。