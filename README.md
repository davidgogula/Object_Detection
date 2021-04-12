# Object_Detection

# YOLO V3 Steps to implement:
 * Using LabelImg , label all your images
 * Compress all your  Images(custom data) along with corresponding .txt files
 * Upload it to google drive.
 * Mount your collab notebook with google drive and unzip data
 * yolo uses darknet on the background,so you need to clone darknet repo
 * After that create a makefile (compling your model) and modify the below
    GPU = 1
    CUDNN = 1
    OPENCV = 1
    
 * Copy files in yolov3_files to data folder in drive. And modify 
    full_path_to_images to folder name of dataset
 * Modify classes.txt and classes.names file
 * Run both these .py files , then you get test.txt and train.txt and labelled_data.data files
 * Create custom_weight folder in drive, to store weights of pre-trained model(Transfer Learning)
 * Modify configuration files in darknet/cfg
 * create backup folder to store final_weights 
 * Command to  train our model 
  !darknet/darknet detector train custom_data/labelled_data.data darknet/cfg/yolov3_custom.cfg 
custom_weight/darknet53.conv.74 -dont_show

* command to check performance of our model
 !darknet/darknet detector map custom_data/labelled_data.data darknet/cfg/yolov3_custom.cfg 
backup/yolov3_custom_1000.weights -dont_show

  

