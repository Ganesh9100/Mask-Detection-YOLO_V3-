
Training with yolov3

 Create the DataSet of near atleast 300 per class 


For Creating Bounding Box and Annotation file  you can use below tools 

in C++: https://github.com/AlexeyAB/Yolo_mark

in Python: https://github.com/tzutalin/labelImg

in Python: https://github.com/Cartucho/OpenLabeling

in C++: https://www.ccoderun.ca/darkmark/

in JavaScript: https://github.com/opencv/cvat


After creating the DataSet ,
You have to create 3 different file's
 Create the Image names with train.txt with directory build\darknet\x64\ , Example build\darknet\x64\image_01.jpg 
 Create file obj.names in the directory build\darknet\x64\data\, with objects names - each in new line
 Create file obj.data in the directory build\darknet\x64\data\, containing (where classes = number of objects):
 
 Example :( obj.data )
 
  classes= 2
  
  train  = data/train.txt
  
  valid  = data/test.txt
  
  names = data/obj.names
  
  backup = backup/
  
  Clone the github page : 
  https://github.com/AlexeyAB/darknet
  
  Modify the Make File and Compile it 
  
  
  Make sure that you have copy of the Dataset under Darknet or Darknet/data
  
  Download the Pre-trained weights based on the Algorithm you use , for yolov3 - https://pjreddie.com/media/files/darknet53.conv.74
  
  Modify the cfg file with respective the Algorithm and the dataset and Compile it befor Training 
  
  Train the Model using : Example 
  
      ( Windows ) darknet.exe detector train data/obj.data yolov4-tiny-obj.cfg yolov4-tiny.conv.29 
               
      ( Linux )   !./darknet.exe detector train data/obj.data yolov4-tiny-obj.cfg yolov4-tiny.conv.29
  
  Stop the Training,
  
  When you see that average loss 0.xxxxxx avg no longer decreases at many iterations then you should stop training. The final avgerage loss can be from 0.05 (for   a small model and easy dataset) to 3.0 (for a big model and a difficult dataset).
  
  Or Choose weights-file with the highest mAP (mean average precision) or IoU (intersect over union)
  
  
For example, you stopped training after 9000 iterations, but the best result can give one of previous weights (7000, 8000, 9000). It can happen due to          overfitting. Overfitting - is case when you can detect objects on images from training-dataset, but can't detect objects on any others images. You should get weights from Early Stopping Point:



Example of custom object detection: darknet.exe detector test data/obj.data yolo-obj.cfg yolo-obj_8000.weights



 My Model Summary :
 
 

<b> Mask_Not_Detected</b>
<p align="left">
  
  <img src="https://github.com/Ganesh9100/Mask-Detection-YOLO_V3-/blob/master/download1.png" width="250" title="hover text">
  
</p>
<b> Mask_Detected</b>
<p align="left">
  
  <img src="https://github.com/Ganesh9100/Mask-Detection-YOLO_V3-/blob/master/download2.png" width="250" title="hover text">
  
</p>

<b><s> Model_Summary</s></b>
<p align="left">
  
  <img src="https://github.com/Ganesh9100/Mask-Detection-YOLO_V3-/blob/master/summary.jpeg" width="450" title="hover text">
  
</p>



<p>
 <b>class_id = 0, name = Mask_Detected , ap = 98.04% (TP = 681, FP = 29)</b>
 
 <b>class_id = 1, name = Mask_Not_Detected, ap = 96.70% (TP = 385, FP = 18)</b>

for conf_thresh = 0.25, precision = 0.96, recall = 0.96, <b>F1-score = 0.96</b>

for conf_thresh = 0.25, TP = 1066, FP = 47, FN = 40, <b>average IoU = 71.77 %</b>

IoU threshold = 50 %, used Area-Under-Curve for each unique Recall
<b>mean average precision (mAP@0.50) = 0.973706, or 97.37 %</b>
Total Detection Time: 33 Seconds

</p>




 
