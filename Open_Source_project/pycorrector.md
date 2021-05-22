# pycorrector

1. kenlm
    - kenlm统计语言模型工具，规则方法，语言模型纠错，利用混淆集，扩展性强。
    - 测试效果如下：

        ![image](docs/kenlm.png)

        - 结果不够理想，只能找到一个简单错误“桥礅”。


2. macbert
    - 来自哈工大SCIR实验室2020年的工作，改进了BERT模型的训练方法，使用全词掩蔽和N-Gram掩蔽策略适配中文表达，和通过用其相似的单词来掩盖单词，从而缩小训练前和微调阶段之间的差距。
    - 测试效果如下：

        ![image1](docs/macbert.png)
        
        - 效果差，没有找出任何错误。
        
        
3. bert
    - 中文文本fine-tuned3轮后的预训练BERT MLM模型。
    - 纠错效果可圈可点，优于kenlm模型，并且识别出来的都是真正的错误。
        
        ![image](docs/bert.png)

4. ernie
    - [ERNIE](https://github.com/PaddlePaddle/ERNIE)是百度开创性提出的基于知识增强的持续学习语义理解框架，该框架将大数据预训练与多源丰富知识相结合，通过持续学习技术，不断吸收海量文本数据中词汇、结构、语义等方面的知识，实现模型效果不断进化。
    - 测试效果可圈可点，效果于bert相当。
        
        ![image](docs/ernie.png)



        
        