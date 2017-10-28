# Focal-Loss-implement-on-Tensorflow
  This is the implementation(unofficial version) of focal loss proposed on <a href ="https://arxiv.org/abs/1708.02002">Focal Loss for Dense Object Detection</a> by KM He.
  After implement focal loss formular I have tested on SSD_MobileNet Network on COCO datasets. The following is about the tensorboard results and analysis:
  1. The map@0.5 of focal loss implementation(num_hard_example=20000, max_neg_per_pos=1000, max_total_detection=20000) are about 3% higher than original model(num_hard_example=2000, max_neg_per_pos=100, max_total_detection=100), about 29% and 26% respectively.
  
  ![MAP and Loss](https://github.com/ailias/Focal-Loss-implement-on-Tensorflow/blob/master/map_res.png)
  ![MAP of some cates](https://github.com/ailias/Focal-Loss-implement-on-Tensorflow/blob/master/map_some.png)
  
  2. However, why do focal loss can achive so much improvement?  Here we show some evaluation images and then we may find the answer. Focal loss do not detect the low percentage object, this may have a good precision but bad recall. But the core viewpoint of the paper is focals on the hard examples while ignore the easy examples. I don't know the reason.
  
  ![Eval image result comp](https://github.com/ailias/Focal-Loss-implement-on-Tensorflow/blob/master/img_res.png)

  Conclusion: Maybe Focal loss can have a better precision(MAP) but may have worse recall.(personal opinion)
