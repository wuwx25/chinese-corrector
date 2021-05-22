# 开源项目
1. [pycorrector](https://github.com/shibing624/pycorrector)，一个中文文本纠错开源工具。音似、形似错字（或变体字）纠正，可用于中文拼音、笔画输入法的错误纠正，测试效果可见[文档](http://192.168.0.202/wuwx/chinese-corrector/-/blob/master/Open_Source_project/pycorrector.md)。


2. 基于bert的中文文本纠错[项目](https://github.com/JohanyCheung/bert_chinese)。
    
    - 使用bert的mask language model预测一句话中的某个字，取前5个最有可能的结果。
    - 如果预测的结果是原来的字则忽略，如果不是原来的字，就用pypinyin检测和原来的字拼音相似的结果作为纠正结果。 
    - 测试效果可见[文档](url)。