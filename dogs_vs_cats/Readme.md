train_dogs_cats.ipynb
- ImageDataGenerator有使用augmentation, 幾乎所有transform都用上了
- 使用resnet50當feature extractor, 再接上GlobalAveragePooling2D跟Dense輸出2個output
- 因為data量很多，所以steps_per_epoch設100，不過即使跑很多epoch, loss大約就是停留在0.1上下, kaggle上其他人是可以降到0.05-0.06的
- 這樣train完的validation accuracy=0.97

test_dogs_cats.ipynb
- 使用clip來讓分類的分數不要太極端，可以稍微增加test score, [0.02, 0.98]
- 上傳test的結果名次只有大約一半的排名(650/1314, score=0.12x左右)

todo
- 看論壇上說training data裡面有一些資料的分類是錯誤的，要先手動處理這些
- 對learning rate的調整要再多看看別人怎麼用
- ensemble看起來是可以有效提升分數
