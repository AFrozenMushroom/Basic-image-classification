# Basic-image-classification-简单的服装图像识别
使用tensoflow和keras构造的图像识别模型，可以识别十种服装
使用fashion-mnist数据集为训练用数据
make-model为制作模型的程序，包括载入数据，简单数据处理，编撰模型，训练模型，评估模型和保存模型
运行make-model，会生成模型文件my_model.keras。同时返回模型的准确率，约为88%左右
use-model为对模型的使用，包括调用模型my_model.keras。并将fashion-mnist数据集的测试集代入，生成预测结果
运行use-model，随即返回fahion-mnist测试集中的一张照片，照片写有其类和预测的类别
本模型可识别的服装有‘T恤/上衣', '裤子', '套头衫', '连衣裙', '外套','凉鞋', '衬衫', '运动鞋', '包', '短靴'十种，分别对应类别0-9
本模型采用一个fatten层将数据展平为一维，两个全连接层生成参数。最终每张照片返回十个数字，最大的对应位置为预测类别
本模型采用adam最优化方法，损失函数为交叉熵，评估标准为accuracy
