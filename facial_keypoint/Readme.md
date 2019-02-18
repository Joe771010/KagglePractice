% training data不是每個人臉都有完整的特徵點 %

train_facial_keypoints.ipynb
- 只取有完整特徵點的人臉來train
- 有做pre-processing(zero-center, normalization)
- regression的問題，最後一層是用linear activation function
- (參考別人的作法)不需用到複雜的network, 用幾層Conv2D與Pooling即可, BatchNormalization也不用(BN應該是很深的時候才發揮效用?)
- 這樣做完的test score=3.2, 排名大約是70/175

train_facial_keypoints2.ipynb
- 拿之前train出來的model來算出有缺點的training data, 填上去
- 取所有完整的training data來重新train
- 分數進步到2.48, 排名大約是51/175
