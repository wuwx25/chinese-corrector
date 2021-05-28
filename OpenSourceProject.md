# 开源项目
1. [pycorrector](https://github.com/shibing624/pycorrector)，一个中文文本纠错开源工具。音似、形似错字（或变体字）纠正，可用于中文拼音、笔画输入法的错误纠正，测试效果可见[文档](http://192.168.0.202/wuwx/chinese-corrector/-/blob/master/Open_Source_project/pycorrector.md)。


2. 基于bert的中文文本纠错[项目](https://github.com/JohanyCheung/bert_chinese/blob/master/corrector/README.md)。
    
    - 使用bert的mask language model预测一句话中的某个字，取前5个最有可能的结果。
    - 如果预测的结果是原来的字则忽略，如果不是原来的字，就用pypinyin检测和原来的字拼音相似的结果作为纠正结果。 
    - 测试效果可见[文档](http://192.168.0.202/wuwx/chinese-corrector/-/blob/master/Open_Source_project/bert_chinese.md)。


3. HeadFilt
    - 该论文是学术界的一篇中文纠错论文，在中文公开纠错数据集上取得了不错的效果。
    - 纠错模块分两部分：第一部分是基于bert的base模型，输出可能纠错后的结果，第二部分是一个filter模块，主要基于treeLSTM模型学习出字的hierarchical embedding，通过向量相似度衡量两个字的相似度，取代了预先设定好的混淆集并且可以通过模型的自适应学习，发现字与字之间新的混淆关系能力，通过filter模块，进一步过滤bert模型的过纠等问题，提高准确率。
    - 测试效果可见[文档](http://192.168.0.202/wuwx/chinese-corrector/-/blob/master/Open_Source_project/HeadFilt.md)