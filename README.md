# Yolo Mixed Backbone

## Download dataset images and annots

[UCF and JHMDB](https://pan.baidu.com/share/init?surl=HSDqKFWhx_vF_9x6-Hb8jA)


## Download weight

[Imagenet](https://pan.baidu.com/share/init?surl=BP7X222ZPqOndbojwOPjkw)

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