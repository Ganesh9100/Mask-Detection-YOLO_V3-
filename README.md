
Training with yolov3
Step 01: Create the DataSet of near atleast 300 per class 
For Creating Bounding Box and Annotation file  you can use below tools 

Here you can find repository with GUI-software for marking bounded boxes of objects and generating annotation files for Yolo v2 - v4: https://github.com/AlexeyAB/Yolo_mark

Different tools for marking objects in images:

in C++: https://github.com/AlexeyAB/Yolo_mark
in Python: https://github.com/tzutalin/labelImg
in Python: https://github.com/Cartucho/OpenLabeling
in C++: https://www.ccoderun.ca/darkmark/
in JavaScript: https://github.com/opencv/cvat

I have used LabelImg for creating Bounding Boxes
After creating the DataSet ,
You have to create 3 different file's
 Create the Image names with train.txt with directory build\darknet\x64\ , Example build\darknet\x64\image_01.jpg 
 Create file obj.names in the directory build\darknet\x64\data\, with objects names - each in new line
 Create file obj.data in the directory build\darknet\x64\data\, containing (where classes = number of objects):
 
 Example :
  classes= 2
  train  = data/train.txt
  valid  = data/test.txt
  names = data/obj.names
  backup = backup/
 
