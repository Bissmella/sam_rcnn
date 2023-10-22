# SAMDet

samDet is an "attempt" to extend segment anything with a small extension for detection head following RCNN method.

# Dataset
VEDAI dataset is used and to make the training process quick the dataset have already been pre-processed by SAM-b and the encoded image-features and the masks have been stored in .npy and text files. Pre-processed data is avaiable at: https://drive.google.com/drive/folders/12ZcQeC_knOVRW1uUkOFiJYP6d4-PPnrT?usp=sharing  
If you wish to use a larger version of SAM, the features and masks can be produced from scratch easily by loading SAM model and going through all images and saving the SAM's image encoder output and output of automatic mask generator of SAM.

To train the model:  
-Download the VEDAI dataset from: https://downloads.greyc.fr/vedai/  
-Download pre-processed SAM features and masks from https://drive.google.com/drive/folders/12ZcQeC_knOVRW1uUkOFiJYP6d4-PPnrT?usp=sharing  
-Run data-transform.py to create the correct file paths for each 10 folds  
The datset folders should have a structure like:  
  ├──VEDAI  
      ├──images  
      ├──labels  
  ├──VEDAI_1024  
      ├──images  
      ├──labels  
      ├──features  
      ├──masks  


## Citation

-@article{kirillov2023segany,
  title={Segment Anything},
  author={Kirillov, Alexander and Mintun, Eric and Ravi, Nikhila and Mao, Hanzi and Rolland, Chloe and Gustafson, Laura and Xiao, Tete and Whitehead, Spencer and Berg, Alexander C. and Lo, Wan-Yen and Doll{\'a}r, Piotr and Girshick, Ross},
  journal={arXiv:2304.02643},
  year={2023}
}

-Fast-RCNN
-Yolov5
-@ARTICLE{10075555,
  author={Zhang, Jiaqing and Lei, Jie and Xie, Weiying and Fang, Zhenman and Li, Yunsong and Du, Qian},
  journal={IEEE Transactions on Geoscience and Remote Sensing}, 
  title={SuperYOLO: Super Resolution Assisted Object Detection in Multimodal Remote Sensing Imagery}, 
  year={2023},
  volume={61},
  number={},
  pages={1-15},
  doi={10.1109/TGRS.2023.3258666}}
