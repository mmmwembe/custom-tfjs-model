# custom-tfjs-model

Trying to load custom tensorflowjs model instead of the mobilenet model
The custom model is trained to classify Pinochle cards. Test images are in the /test-images directory
The tensorflowjs model is contained in directory: /custom-tfjs-model
The labels are in LABELS.js


Tried changeing the detect.js script in Juande's tutorial https://github.com/juandes/tensorflowjs-objectdetection-tutorial

changed the line below:
```
      const loadlModelPromise = cocoSsd.load();
```

to: 
```
      const  loadModelPromise = tf.loadGraphModel('http://localhost:8000/custom-tfjs-model/model.json')  
```
However this doesn't work...even when I import
```
  import * as tf from '@tensorflow/tfjs';
  
```