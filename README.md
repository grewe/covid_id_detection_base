# covid_id_detection_base is a repository with multiple examples of using Object Detection API in Tensorflow 2

### <font color=blue>Roboflow_TensorFlow2_Object_Detection.ipynb:</font>  is a modification of  https://towardsdatascience.com/how-to-train-a-tensorflow-2-object-detection-model-25d4da64b817  developed to RUN LOCALLY rather than in a colab (see https://colab.research.google.com/drive/1sLqFKVV94wm-lglFq_0kGo2ciM0kecWD#scrollTo=fF8ysCfYKgTP&uniqifier=1).  This example expects the input images and corresponding bounding box information to be stored in a TFRecord format for both training and validation.  For testing raw images are also expected in a raw_data subdirectory (read notebook)
- NOTE the original reports (see url above) issue with tf_utils.py file which is overwrites and as such <font color=red>should be run in its own isolated conda environment as it changes the base TF2 file</font>


### <font color=blue> eager_few_shot_od_training_tf2_colab.ipynb :</font>  is a modification of [official Object Detection API page](https://blog.tensorflow.org/2020/07/tensorflow-2-meets-object-detection-api.html?m=1) to retrain a model that allows for multiple classes loading the image and corresponding bounding box information into arrays and then converting to tensors for presentation in retraining of a TF Model.  This example expects the images for training, validation and testing data to be located in a data/images folder.   It expects that for each image an xml file indicating the bounding box(es) will be present of name imageName.xml and located in data/train_labels and data/test_labels for use in training and testing respectively (this is how you effectively choose which images will be training and will be testing). It also expects a label_map.pbtxt that will contain the list of classes and their category numbers and display names.   
- This script will produce a csv file called train_labels.csv and test_labels.csv and turn this ALONG WITH THE IMAGE DATA into  single TFRecord files train_labels.record and test_labels.record respectively. 
- [Official Object Detection API for TF2 page](https://blog.tensorflow.org/2020/07/tensorflow-2-meets-object-detection-api.html?m=1)
- [Original jupyter notebook example - 1 class](https://github.com/TannerGilbert/Tensorflow-Object-Detection-with-Tensorflow-2.0)
- Install the Object Detection API Models directory on your system and the original file will be located in WHATEVER\INSTALL_DIR\models\research\object_detection\colab_tutorials


### <font color=blue> object_detect_tutorial.ipynb :</font>  is a modification of the prediction example script from the [official Object Detection API page](https://blog.tensorflow.org/2020/07/tensorflow-2-meets-object-detection-api.html?m=1) that simply loads a model and runs predictions agains a set of test images stored in a testing folder
- [Official Object Detection API for TF2 page](https://blog.tensorflow.org/2020/07/tensorflow-2-meets-object-detection-api.html?m=1)
- [Original jupyter notebook example - 1 class](https://github.com/TannerGilbert/Tensorflow-Object-Detection-with-Tensorflow-2.0)
- Install the Object Detection API Models directory on your system and the original file will be located in WHATEVER\INSTALL_DIR\models\research\object_detection\colab_tutorials

