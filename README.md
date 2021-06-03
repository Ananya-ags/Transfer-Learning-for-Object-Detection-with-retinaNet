# Transfer-Learning-for-Object-Detection-with-retinaNet

Project Description:
In this project, a pre-trained classifier was leveraged for its feature extraction capabilities and then retrained it on a small set of images (in this case 5 images of a rubber duck) to create a tight bounding box around the new object.

The TensorFlow model Garden was used with the Object Detection API. The pre-trained weights of the RetinaNet were used for all layers but the classification head, which was randomly intitialised and then fine-tuned on 5 images of the rubber-duck. The Adam Optimization algorithm was used while fine-tuning to minimize the loss on this novel class. (Novel as the RetinaNet was originally trained on the COCO dataset, which does not contain rubber ducks or any ducks). 

The fine-tuning when accelerated by GPU was completed under 2 mins, and the model did a decent job at making inference on test-images (considering that only 5 images had been used for retraining the model to detect a novel class)
 
