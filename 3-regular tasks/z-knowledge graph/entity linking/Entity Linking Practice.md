定义：

消歧本质上，就是含义不同的实体，其表示(representation)也不同.

提供的信息 - 

1. 知识库中的歧义实体，根据描述信息，可以得知各个实体是唯一的，关键在于获得其表示（使其变得可计算）. 同时，任意输入文本所获得的实体表示，能够对应到知识库中的实体表示，意味着两者必须共享一个表示空间！

2. 标注数据中的实体

   实体之间的关系也可能有利于区分歧义实体，这种关系占比多少？可能不是重点！

如何利用这两方面的信息？





解决方案：

方案一

bert + finetuning

第一次 finetuning， 获得学习知识库的实体表示

第二次 finetuning，获得分类结果



方案二

将知识库信息看作外部信息

1. 知识表示
2. 规则

二分类模型 + 外部信息

在二分类模型的embedding中，拼接知识库实体的知识表示及规则。





基于匹配的框架

要求：

要求两个实体对齐（即匹配时，要模型知道重点是在匹配两个实体）

方便加入外部特征






