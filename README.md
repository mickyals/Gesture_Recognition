# Gesture Recognition
> Problem Statement
 Imagine you are working as a data scientist at a home electronics company which manufactures state of the art smart televisions.
 You want to develop a cool feature in the smart-TV that can recognise five different gestures performed by the user which will help users control the TV without using a remote.
 
 The gestures are continuously monitored by the webcam mounted on the TV. Each gesture corresponds to a specific command:
 Thumbs up:  Increase the volume
 Thumbs down: Decrease the volume
 Left swipe: 'Jump' backwards 10 seconds
 Right swipe: 'Jump' forward 10 seconds
 Stop: Pause the movie
 
 |Gesture|Response|
 |-------|--------|
 |Thumbs up| Volume up|
 |Thumbs down| Volume down|
 |Left swipe| backward - 10 secs|
 |Right swipe| forward - 10 secs|
 |Stop| Pause|
 
 Each video is a sequence of 30 frames.
 
 
 
## Goal
> To develop a deep learning model that is capable of classifying different gestures.
 
 
## Dataset
> The dataset for this model can be retreieved from the [link](https://drive.google.com/uc?id=1ehyrYBQ5rbQQe6yL4XbLWe3FMvuVUGiL). The training dataset consists of hundreds of videos with their ground truths noted.
 
 
## Approach
> The general approach taken is one of experimentation with the varying of a single parameter or aspect of the network and comparing it to previous runs. The overall goal is to build a relatively accurate gesture recognition model and see how these varying paramters affect performance.
 
 
## Results
> With custom architecture using a few skip connects, the best model is capable of a validation accuracy of 85-90%. This model performed similarly to ResNet with 50% of its layers trainable.


## Conclusion
> Batch Size, the choise of optimizer, the position of normalisation layers, dropouts, pool size and more have significant effects on the performance of any model. Using custom architectures requires rigorous experimentation and evaluation. HOwever, these models are limited solely to the dataset they were trained on and therefore likely will not perform well in real world scenarios. However, transfer learning models are able to give a more than random chance result on the dataset even though theu were not trained on such which goes to show the versatility of established models such as ResNet. While new architectures are necessary in some cases, using and improving upon a pre-built model and architecture provides a good benchmark to test your model AND a fast and easy way to bring a new system to production. 