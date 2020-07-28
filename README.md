# covid_id_detection_base is a repository with multiple examples of using Object Detection API in Tensorflow 2

### <font color=blue>Roboflow_TensorFlow2_Object_Detection.ipynb:</font>  is a modification of  https://towardsdatascience.com/how-to-train-a-tensorflow-2-object-detection-model-25d4da64b817  developed to run locally rather than in a colab (see https://colab.research.google.com/drive/1sLqFKVV94wm-lglFq_0kGo2ciM0kecWD#scrollTo=fF8ysCfYKgTP&uniqifier=1)
- NOTE the original reports (see url above) issue with tf_utils.py file which is overwrites and as such <font color=red>should be run in its own isolated conda environment as it changes the base TF2 file</font>



### <font color=blue> eager_few_shot_od_training_tf2_colab.ipynb :</font>  is a modification of that allows for multiple classes loading the image and corresponding boudning box information into an arrays and then converting to tensors for presentation in retraining of a TF Model. 
