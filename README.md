# CoronaMask-Detection
Mask Detection in Real-time with 99% Accuracy

# Demo Video

<video>https://www.youtube.com/watch?v=ErVbWTY_Rz4</video>

# Linkedin Post 
https://www.linkedin.com/posts/kushal-dulani-28145a189_artificialintelligence-ai-covid19-activity-6659385898809073664-mEB7

# After Lot's of request i'm making this as an open source , if i found this used in monitized by any type , all the legal action will done by me

#### I will publish blog on it that How to make these type of object detection from Scratch and also share labeled images

#### Please Give Star to My Repository For My Work and I will upload all industrial/Real-Life projects for you, Thank You

#### Subscribe My YouTube Channel - AI Developer Kushal and Follow me on Instagram @ai.developer_kushal , After 1000 Subscriber and Followers I'll make tutorial videos from scratch in English/Hindi for lot's of project and it'll be absolutely FREE, hurry up!

### i can't upload files on github because of memory limit that's why i'm sharing my drive link
https://drive.google.com/drive/folders/1mzJPZb1R5ogtT9nC_TL0MY2VGTcly4Nz

# Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.


# How to Use

## if you are using anaconda then create new environment for easy of use

1)conda create --name mask

2)conda activate mask

then install requirments


# Prerequisites

opencv,
matplotlib,
Cython,
contextlib2,
pillow,
lxml,
tensorflow,
jupyter notebook 

# Installing

pip install  opencv-python

pip install  opencv-contrib-python

pip install  Cython

pip install  contextlib2

pip install  pillow

pip install  lxml

pip/conda install  jupyter

pip/conda install  matplotlib

pip/conda install  tensorflow-gpu==1.15 <-- "Note i used 1.15 version for cuda enable gpu"

### if you don't have Nvidia Graphics which compatiblity >5.0 or AMD Graphics
### you can use cpu version

pip/conda install  tensorflow==1.15 <-- "Note i used 1.15 version for cpu"



(step-1) Download tensorflow object detection api model from github "https://github.com/tensorflow/models"

(step-2) Goto models/research/object_detection and change protos folder with my protos folder then run in terminal " ./bin/protoc object_detection/protos/*.proto --python_out=. "  <-- without inverted comma

(step-3) Goto models/research and run command "python setup.py" build then run "python setup.py install"  <-- without inverted comma


(step-4) Goto models/research/slim change file name BUILD to BUILDD

(step-5) Goto models/research/slim and run command "python setup.py build" then run "python setup.py install"  <-- without inverted comma


(step-6) Goto models/research/object_detection and paste inference_graph,training,run.py,train.record,test.record and finalmask.mp4

(step-7) open your terminal goto models/research/object_detection and run python run.py

(step-8) if you want to use your own video then change videofile in run.py at line no 89 and you want to use your ip/rtsp camera chnage http/rtsp link at line no 90 and comment line no 89

# (optional) 
if you want to export tflite graph and you can use this command

Goto models/research/object_detection and run

python export_tflite_ssd_graph.py --input_type image_tensor --pipeline_config_path training/ssd_mobilenet_v2_coco.config --trained_checkpoint_prefix training/model.ckpt-43979 --output_directory inference_graph2

now you can check in models/research/object_detection/inference_graph2 in this folder you can fild tflite_graph.pb and tflite_graph.pbtxt files , you can use in micro-computers like rasberrypie/nvidia jetson nano etc 


# Author
#### Kushal Dulani 
