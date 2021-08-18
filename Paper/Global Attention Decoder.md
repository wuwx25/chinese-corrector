### Global Attention Decoder for Chinese Spelling Error Correction详解

在本篇文章中指出，以往的csc方法往往会使用bert等模型来提取局部的上下文信息，从而指导模型如何进行改错，但是，在这些上下文的信息中也会存在着错误的信息。为了解决以上的问题，本文主要提出了两种关于中文改错的新思路。

1. 提出一种新的bert替换策略，与之前的替换不同的是，这种策略是基于混淆集来进行引导的。
2. 提出一个提取全局上下文信息的办法，也就是文中称之为**Global Attention Decoder**的模块。这个模块的作用是学习潜在正确字符和潜在错误字符的候选之间的关系，通过学习更丰富的全局知识，从而达到缓解局部错误信息的干扰。


![global attention decoder的框架](../docs/global%20attention%20decoder.png)

以上这篇文章提出的框架图，之后我们将会逐一进行分析。

####Bert_CRS

