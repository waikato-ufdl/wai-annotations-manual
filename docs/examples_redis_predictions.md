[Redis](https://redis.io/) is a fast, in-memory data store, which can be used
as a database, cache, streaming engine, and message broker. It is a great way
of incorporating deep learning frameworks that are run from within 
[Docker](https://www.data-mining.co.nz/docker-for-data-scientists/) containers,
simplifying the dependencies due to decoupling. 

wai.annotations has support for the following data domains:

* **image classification**: sends image, receives JSON with label/probability pairs
* **object detection**: sends image, receives JSON in [OPEX](https://github.com/WaikatoLink2020/objdet-predictions-exchange-format) format
* **image segmentation**: sends image, receives segmented image (indexed PNG or blue-channel PNG)

# Docker images

The following Docker images are available for connecting to the prediction plugins:

* Image classification

    * [PyTorch](https://github.com/waikato-datamining/pytorch/tree/master/image-classification)
    * [Tensorflow](https://github.com/waikato-datamining/tensorflow/tree/master/image_classification)

* Object detection

    * [Detectron2](https://github.com/waikato-datamining/pytorch/tree/master/detectron2)  
    * [Yolov5](https://github.com/waikato-datamining/pytorch/tree/master/yolov5)
    
* Image segmentation

    * [Image segmentation Keras](https://github.com/waikato-datamining/tensorflow/tree/master/image-segmentation-keras)
