CBOWDataset 类：
处理文本数据并构建词汇表
实现了mask_index和unk_index特殊标记
提供了add_token方法的基础功能
自动处理 context 和 target 的生成
确保每个 context 的分词后的词数一致
CBOWVectorizer 类：
基于 PyTorch 实现的神经网络模型
使用 Embedding 层将单词转换为向量
实现了 context 词向量的求和操作
输出层预测目标词
训练流程：
使用 DataLoader 批量加载数据
设置模型为训练模式并应用 Dropout
使用 Adam 优化器
支持指定最大训练轮数
设备与随机种子：
支持 GPU 训练检测
包含随机种子设置（代码中预留了位置）
推理与测试：
提供获取目标词向量的接口
支持模型评估模式
关键参数：
embedding_size 可配置
包含默认参数值设置
支持模型优化配置
这个实现完整覆盖了 Word2Vec 的 CBOW 模型核心功能，包括数据处理、模型构建、训练和推理过程。
