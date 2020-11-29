I have trained the model with 2 class of images [ Mask_detected and No_Mask detected] ,Where I ran my model in Google Colab till 1300 iteration which gives me the Highest Accuracy when training with 1113 images .  

Upload the below files to darknet/data directory : For training 

   train.txt
   obj.names
   obj/data
   dataset 
   test.txt ( optional )
 
 After training use the best weight file for detection .
 
 Further Resource : https://github.com/AlexeyAB/darknet
 

Model Ouput :
 
 

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

[![Watch the video](https://github.com/Ganesh9100/Mask-Detection-YOLO_V3-/blob/master/Screenshot%20from%202020-07-15%2019-46-13.png)](https://youtu.be/NcPq3xSN9vM)

<p>
   <img src="https://github.com/Ganesh9100/Mask-Detection-YOLO_V3-/blob/master/f1.jpeg" width="350" title="hover text">
   
 <b>class_id = 0, name = Mask_Detected (TP = 681, FP = 29)</b>
 
 <b>class_id = 1, name = Mask_Not_Detected (TP = 385, FP = 18)</b>

 precision = 0.96, recall = 0.96, <b>F1-score = 0.96</b>

 TP = 1066, FP = 47, FN = 40, <b>average IoU = 71.77 %</b>

<b>mean average precision (mAP@0.50) = 0.973706, or 97.37 %</b>
Total Detection Time: 33 Seconds

</p>
If you have doubts please inbox me at ganeshraj1999@outlook.com<BR>
Hey, want to implement ?...Here is my blog, https://www.codementor.io/@edugan28/face-mask-detection-using-yolo-v3-18tpxfjrso</p>




 
