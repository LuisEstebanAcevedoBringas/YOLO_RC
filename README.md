# Yolo Mixed Backbone

## Download dataset (images and annots) and weights

https://drive.google.com/drive/folders/1-CyMU793yB98X86FUNt_3ntMFZasd1Qw

## Extra configs

1) Yaml
   1) Change the clip size on the var "clip size"
   2) Change the parameter 4 on the last Conv_3D to the same value as the var "clip size"
2) On the train change in the function "parse_opt":
   1) "--name" change it according the experiment
   2) "--cfg", make sure that is the same name as the yaml file
   3) "--data", put the path to the data set
   4) "--epochs" is set to 30 epochs but it can be changed
   5) "--batch-size" change it according to the gpu
   6) "--workers" change it according to the gpu
   7) "--device" change it according the gpu you want to use
3) torch_utils.py:
   1) Line 286 change the temporal kernel to plot the GFLOPs
4) Dataloader3D.py
   1) Lines 1395, 1432 and 1489: Put the rgb-images path of the dataset that you want to use
   2)  Lines 795, 1394, 1430 and 1485 change it for the name of the dataset that you want to use
5) val.py
   1) "--data" change to the yaml of the dataset that you want to use
   2) "--weights" change it to the weights that you want to use 

## Eval config
1) Dataloader3D.py
   1) Lines 1395, 1432 and 1489: Put the "rgb-images" path of the dataset that you want to use
   2)  Lines 795, 1394, 1430 and 1485 change it for the name of the dataset that you want to use ("ipn", "jhmbd" or "ucf")
2) val.py
   1) "--data" change to the yaml of the dataset that you want to use
   2) "--weights" change it to the weights that you want to use
3) ucf.yaml
   1) Change the paths of "train", "val" and "test" 
