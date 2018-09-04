1. Please download the caffe AlexNet model for feature extraction from the the link https://www.dropbox.com/sh/owk9wljp2vipwkk/AADQlsSzm9jMEScxYTQ57mUGa?dl=0&lst=

2. Two files in AlexNetFC6Extract are listed as follows:

    (1) bvlc_reference_caffenet.caffemodel
    (2) deployModify.prototxt
    
3. Install loadcaffe according to the instruction from https://github.com/szagoruyko/loadcaffe  

4. load pre-trained AlexNet on ImageNet and extract FC6 features for your own image data. The below code is the reference.
 ```
    alexnet = CaffeLoader.load('./deployModify.prototxt','./bvlc_reference_caffenet.caffemodel')
    print(alexnet)
    alexnet:remove()
    alexnet:remove()
    alexnet:remove()
    alexnet:remove()
    alexnet:remove()
    alexnet:remove()
    print(alexnet)
 ```
